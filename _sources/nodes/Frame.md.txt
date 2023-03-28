
# Node Frame

Node *Frame*

Args:
  label: The frame label
  label_size: The font size for the label
  color: A valid color spec
  shrink: Shrink the Frame
  
Note that *Frame* is the internal name for *Layouts*

<sub>Blender reference : [NodeFrame](https://docs.blender.org/api/current/bpy.types.NodeFrame.html)</sub>




## \_\_init\_\_

Node *Frame*

Args:
  label: The frame label
  label_size: The font size for the label
  color: A valid color spec
  shrink: Shrink the Frame
  
Note that *Frame* is the internal name for *Layouts*

<sub>Blender reference : [NodeFrame](https://docs.blender.org/api/current/bpy.types.NodeFrame.html)</sub>




## get_label

Build the node label

If the label provided at initialization time is None, the node is labeled by concatening
its unique id with its standard name.



## children

The nodes within the frame


## capture_inputs

Capture the inputs
replace all the links from group input to one node internally by a
link with a new instance of group input

Note : deals only with blender nodes and links
It is transparent for the script

