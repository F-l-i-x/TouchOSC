## BPM counter example/module

Calculate a simple mean BPM values from a ring buffer of meassured times between button presses. Button blinks in sync with onset. Single taps will be ignored.

![delayed osc](pics/preview.gif)



```lua

local label = self.parent.children.label1
local last = getMillis()
local onset = last
local ring = {0, 0, 0, 0, 0}  -- the ring buffer list we will write the times into
local i = 1
local avg = 0

function init()
  -- restore avg from tag on start, so button blinks with last bpm
  avg = tonumber(self.tag)
end

function onValueChanged(key)
  -- when touch down
  if key == 'touch' and self.values.touch == true then
  
    -- store delta time 
    local deltaT = getMillis() - last
    
    -- update old time
    last = getMillis()
    
    -- only count a beat if time difference is smaller 2 sec.
    if deltaT < 2000 then   
  
      -- store onset for blinking
      onset = last
      
      -- write time difference into the ring buffer list
      ring[i] = deltaT
      
      -- use modulo to get a looping index
      i = (i % 5) + 1
      
      avg = 0
      local realTap = 0
      -- calculate the current average of the ringbuffer
      for j = 1,#ring do
        if ring[j] > 20 then
          avg = avg + ring[j]
          realTap = realTap + 1
        end
      end
      avg = avg / realTap
      
      -- save new avg to tag
      self.tag = avg
      
      -- apply value to label, round to one decimal place and calculate BPM from milliseconds
      label.values.text = math.floor( 60000 / avg * 10 )/10 .. " bpm"

    end
  end
end


function update()
  local now = getMillis()
  
  -- check if button is on and blink time has passed to turn it off
  if self.values.x == 1 and (now - onset ) > 120 then
    self.values.x = 0
    
  -- otherwise check for passed bpm time and turn on
  elseif (now - onset) >= avg then
    self.values.x = 1
    -- update onset time
    onset = now
  end
end

```

---
