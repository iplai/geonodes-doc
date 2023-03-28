
# Data socket Image

> Inherits from dsock.Image
  
<sub>go to [index](../index.md)</sub>



## Methods

- [switch](#switch) : output (Image)

## switch
```{eval-rst}
Geometry node [*Switch*].


  Args:
    switch: Boolean
    true: Image
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Image
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Switch`
  
  - input_type = 'IMAGE'
    
  Blender reference : `GeometryNodeSwitch <https://docs.blender.org/api/current/bpy.types.GeometryNodeSwitch.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Switch(false=self, switch=switch, true=true, input_type='IMAGE', label=node_label, node_color=node_color)
    
```