## ![find() and findAll() to create references to single or multiple objects](find&findAll.tosc)

### ![Grid_label.tosc :](Grid_label.tosc) 

This example shows how to use use the different 'find' functions.

![find](pics/preview.png) 

The 'findAll' returns a list of all found elements that can be iterated over.

![script1](pics/script.png)

'find' and 'findAll' accept an optional boolean parameter, that will make the search descending recursively into all child elements from where it was called. Combining the recursive with the 'root' reference will allow for a comfortable and complete template wide search from any point in your template.

![script2](pics/script2.png)
