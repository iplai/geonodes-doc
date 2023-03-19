
# Data socket Volume

> Inherits from gn.Geometry
  
<sub>go to [index](



## Constructors

- [Cube](#cube) : volume (Volume)

## Methods

- [to_mesh](#to_mesh) : mesh (Mesh)

## Cube
```{eval-rst}
Geometry node [*Volume Cube*].


  Args:
    density: Float
    background: Float
    min: Vector
    max: Vector
    resolution_x: Integer
    resolution_y: Integer
    resolution_z: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Volume
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VolumeCube`
  
  
  Blender reference : `GeometryNodeVolumeCube <https://docs.blender.org/api/current/bpy.types.GeometryNodeVolumeCube.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VolumeCube(density=density, background=background, min=min, max=max, resolution_x=resolution_x, resolution_y=resolution_y, resolution_z=resolution_z, label=node_label, node_color=node_color)
    
```
## to_mesh
```{eval-rst}
Geometry node [*Volume to Mesh*].


  Args:
    voxel_size: Float
    voxel_amount: Float
    threshold: Float
    adaptivity: Float
    resolution_mode (str): 'GRID' in [GRID, VOXEL_AMOUNT, VOXEL_SIZE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Mesh
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VolumeToMesh`
  
  
  Blender reference : `GeometryNodeVolumeToMesh <https://docs.blender.org/api/current/bpy.types.GeometryNodeVolumeToMesh.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VolumeToMesh(volume=self, voxel_size=voxel_size, voxel_amount=voxel_amount, threshold=threshold, adaptivity=adaptivity, resolution_mode=resolution_mode, label=node_label, node_color=node_color)
    
```