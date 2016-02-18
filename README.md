# Repairlish

A repair toolkit, based on a real Pyblish

### Example

Use plug-ins, families and instance to associate fixes and tools to assets.

```python
# Example usage
from maya import cmds
from repairlish import api

class RepairNormals(api.InstancePlugin):
  def process(self, instance):
    for mesh in instance:
      cmds.polyNormalPerVertex(mesh, unFreezeNormal=True)

api.register_plugin(RepairNormals)
```
