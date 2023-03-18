
# Node TransferAttribute

> Geometry node name: [Transfer Attribute](https://docs.blender.org/manual/en/latest/modeling/geometry_nodes/attribute/transfer_attribute.html)<br>
  Blender type: [Transfer Attribute](https://docs.blender.org/api/current/bpy.types.GeometryNodeAttributeTransfer.html)
  
<sub>go to [index](../index.md)</sub>

## Initialization

```python
from geonodes import nodes
node = nodes.TransferAttribute(source=None, attribute=None, source_position=None, index=None, data_type='FLOAT', domain='POINT', mapping='NEAREST_FACE_INTERPOLATED', label=None, node_color=None)
```



## Arguments


### Input sockets

- source : Geometry
- attribute : data_type dependant
- source_position : Vector
- index : Integer

### Parameters

- data_type : str (default = 'FLOAT') in ('FLOAT', 'INT', 'FLOAT_VECTOR', 'FLOAT_COLOR', 'BOOLEAN')
- domain : str (default = 'POINT') in ('POINT', 'EDGE', 'FACE', 'CORNER', 'CURVE', 'INSTANCE')
- mapping : str (default = 'NEAREST_FACE_INTERPOLATED') in ('NEAREST_FACE_INTERPOLATED', 'NEAREST', 'INDEX')

### Node label

- label : Geometry node display label (default=None)
- node_color : Geometry node color (default=None)

## Data type dependant sockets

- Driving parameter : data_type in ('FLOAT', 'INT', 'FLOAT_VECTOR', 'FLOAT_COLOR', 'BOOLEAN')
- Input sockets  : ['attribute']
- Output sockets : ['attribute']   
  
  

## Output sockets

- attribute : data_type dependant

## Data sockets

> Data socket classes implementing this node.
  
  
- [Geometry](sockets/Geometry.md).[transfer_boolean](oolean) : Method
- [Geometry](sockets/Geometry.md).[transfer_color](s/Geometry.md#transfer_color) : Method
- [Geometry](sockets/Geometry.md).[transfer_float](s/Geometry.md#transfer_float) : Method
- [Geometry](sockets/Geometry.md).[transfer_integer](s/Geometry.md#transfer_integer) : Method
- [Geometry](sockets/Geometry.md).[transfer_vector](s/Geometry.md#transfer_vector) : Method
  
