
# Node VertexOfCorner

> Geometry node name: [Vertex of Corner](https://docs.blender.org/manual/en/latest/modeling/geometry_nodes/mesh_topology/vertex_of_corner.html)<br>
  Blender type: [Vertex of Corner](https://docs.blender.org/api/current/bpy.types.GeometryNodeVertexOfCorner.html)
  
<sub>go to [index](index.md)</sub>

## Initialization

```python
from geonodes import nodes
node = nodes.VertexOfCorner(corner_index=None, label=None, node_color=None)
```



## Arguments


### Input sockets

- corner_index : Integer

### Node label

- label : Geometry node display label (default=None)
- node_color : Geometry node color (default=None)

## Output sockets

- vertex_index : Integer
