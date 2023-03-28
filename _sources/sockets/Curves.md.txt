
# Data socket Curves

> Inherits from gn.Geometry
  
<sub>go to [index](../index.md)</sub>



## Methods

- [deform_on_surface](#deform_on_surface) : curves (Curves)

## deform_on_surface
```{eval-rst}

Geometry node [*Deform Curves on Surface*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Curves
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.DeformCurvesOnSurface`
  
  
  Blender reference : `GeometryNodeDeformCurvesOnSurface <https://docs.blender.org/api/current/bpy.types.GeometryNodeDeformCurvesOnSurface.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.DeformCurvesOnSurface(curves=self, label=node_label, node_color=node_color)
    
```