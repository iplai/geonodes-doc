
# Data socket Material

> Inherits from dsock.Material
  
<sub>go to [index](../index.md)</sub>



## Methods

- [selection](#selection) : selection (Boolean)
- [switch](#switch) : output (Material)

## switch
```{eval-rst}
Geometry node [*Switch*].


  Args:
    switch: Boolean
    true: Material
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Material
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Switch`
  
  - input_type = 'MATERIAL'
    
  Blender reference : `GeometryNodeSwitch <https://docs.blender.org/api/current/bpy.types.GeometryNodeSwitch.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Switch(false=self, switch=switch, true=true, input_type='MATERIAL', label=node_label, node_color=node_color)
    
```
## selection
```{eval-rst}
Geometry node [*Material Selection*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.MaterialSelection`
  
  
  Blender reference : `GeometryNodeMaterialSelection <https://docs.blender.org/api/current/bpy.types.GeometryNodeMaterialSelection.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.MaterialSelection(material=self, label=node_label, node_color=node_color)
    
```