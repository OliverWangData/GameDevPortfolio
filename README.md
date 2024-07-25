# Solo Game Development Portfolio

## Common Utility
### CSV data pipeline
Low memory, no-garbage system that allows CSV data to be read and easily accesible in structs. This allows for error checking, easy auto-fill implementations in code, and allows designers to create content without adjusting the codebase.

### Node-based procedural noise
Performant seed generated mathematical procedural noise library with common noise patterns (random, perlin, voronoi, domain warp, fractal, etc...), almost any parameters for that noise (E.g. parameters as minute as changing the subdivision of random grid angles for generating perlin), and even algorithms on that noise (closest neighbour averaging, distance to cells, step / multistep, etc...). Written in shaders (Compute / HLSL), C#, and C++. The C# library allows for node-based creation and chaining of noise. This enables extremely fast prototyping of very complex noises. 

### Notification system
Combines the well integrated UnityEvents (Or other native event systems) with C# delegates to create notifications that are easily hookable, callable, and listenable both in code and using the editor.

### Addressables and async world loading
System that keeps track and loads / unloads assets dynamically based on distance to view frustum. 

- Camera systems
- 
### Dependency-Injection Based Architecture
Many of these systems are written following principles of dependency injection. E.g. any data not authored by the current object is given to the object via constructors, or through the Editor, in it' simplest form (Either the data itself, or the lowest point of reference if changing data is needed). Most references are set up in a "boostrapping" class, which gives every class their dependencies. This gives classes less interconnectedness and the tradeoff is only the boostrapping classes have "hard" references. 



## Survivors Game
High enemy / projectiles count survivors-like gameplay with overworld for effects and unlockables.

<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PYOK/world.png" alt="screenshot of a game" width="100%"/> 

Notable features:
- Unmanaged C#-based collision detection and resolving system that allows for thousands of objects to be colliding and interacting at the same time.

<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PYOK/physics.gif" alt="gif" width="100%"/>
<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PYOK/projectiles.gif" alt="gif" width="100%"/>

- Tile-based tool for reproducible pseudo-random placement of assets. This can be used for GPU-based rendering to enable thousands of instanced assets without low performance impact.

<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PYOK/withoutrendering.png" alt="screenshot" width="100%"/>
<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PYOK/withrendering.png" alt="screenshot" width="100%"/>

- Streamlined asset pipeline where only csv data and the spritesheet asset can create a fully animated game-ready asset with movement / ai, physics, loot, and more. This is done using custom prefabs that can define anything and that are called using the csv data. Allows designers to set up new characters without having to touch the codebase or finick around in engine. 

<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PYOK/pipeline.gif" alt="gif" width="100%"/>

- Powerful and flexible entity behaviour and spawning system that allows mix-and-match behaviours based on simple interface classes. Examples of what it can do:
  - Spawn bullets in any pattern / orientation (cones, radially, sequentially, in parallel, off-screen shapes, etc...)
  - Spawn bullets with any behaviour (homing towards target, circling a target or position, bouncing off entities, oscillating between positions, etc...)
  - Spawn enemies with any logic (Moving straight across the map, running towards player, dodging in patterns, etc...)

<div align="center">
<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PYOK/projectilescode.png" alt="screenshot"/>
<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PYOK/conecode.png" alt="screenshot"/>
</div>

- Shaders using custom HLSL procedural noise libraries or built in particles for effects such as wind.

<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PYOK/worldanim.gif" alt="gif" width="100%"/>
<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PYOK/effects.gif" alt="gif" width="100%"/>


## Block Creator
Level creating / block placing tool with a cartoony art style.

<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/SAND/preview.png" alt="screenshot of a game"/>


Notable features:
- Grid-aligned block placement in a large 3d world.
- In-game node based UI for custom block behaviours.
- Intuitive controls with helpful control guides.
- Smooth, crisp UI for a polished unintrusive feel.

<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/SAND/gameplay.gif" alt="gif of gameplay" width="100%"/>
<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/SAND/nodebehaviour.png" alt="screenshot of a game" width="100%"/>
<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/SAND/previewnight.png" alt="screenshot of a game" width="100%"/>
<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/SAND/previewpink.png" alt="screenshot of a game" width="100%"/>


##  ChunkyChips
Coin pusher game with a large variety of coins, unlockables, balls, etc...

![screenshot of a game](https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/CHCH/preview.png)

Notable features:
- GPU based instanced rendering with carefully tuned physics parameters for high performance with hundreds of on screen coins, all colliding together.
- Smoothly tweened, dynamic, and portrait-mode friendly UI that can be adjusted for a wide array of phone aspect ratios.
- Data-driven formulas and 3d assets that can be used to change values and rewards for game features without having to adjust and recompile code.

<div align="center">
  <img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/CHCH/intro.gif" alt="gif of a new game start"/>
  <img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/CHCH/gameplay.gif" alt="gif of a new game start"/>
  <img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/CHCH/ui.gif" alt="gif of a new game start"/>
</div>


## Adventure Game
Open-World Handcrafted 2D RPG with a cozy overworld feel.

<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/HERMES/preview.png" alt="screenshot of a game" width="100%"/> 

Notable features:
- Powerful **editor tools** to streamline the asset creation process (E.g. a tool that slices spritesheets into unity tiles (static or animated) without overwritting underlying tile assets).

<div align="center">
  <img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/HERMES/tileslicer.gif" alt="gif of slicer tool"/>
</div>


## And Many, Many More Concepts And Prototypes...
<img src="https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PROJ/gameplay.gif" alt="gif of a game" width="100%"/>

![screenshot of a game](https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/ROAD/preview.png)
![screenshot of a game](https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/FLAT/preview.png)
![screenshot of a game](https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/FROG/preview.png)
![screenshot of a game](https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/HPCB/preview.png)
![screenshot of a game](https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/THCH/preview.png)
![screenshot of a game](https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PRCD/preview.png)
![screenshot of a game](https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/MINI/preview.png)
![screenshot of a game](https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PRTO/preview.png)
![screenshot of a game](https://github.com/OliverWangData/GameDevPortfolio/blob/main/Projects/PRAC/preview.png)
