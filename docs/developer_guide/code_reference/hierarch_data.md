`hierarch_data.gd`  contains

- a dictionary called `shapes` that defines all the `SDFShapes`
- a dictionary called `scenarios` that defines the conditions for adding and removing sdfShapes from the world

`scenarios` returns a given scenario 

```mermaid
graph LR
1[Probe collision_set]
2[Probe `Shrink`]
1---3[hierarch]
2---3
3--scenario_selection-->4[hierarch_data.scenarios]
4--scenario_definition-->3

```

collision_set : objects the probe is colliding with. Probe location, basically.

scenarios provide enough data to build out the entire world for a given collision_set