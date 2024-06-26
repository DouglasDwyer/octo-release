# Octo Project

[Try the online demo now.](https://douglasdwyer.github.io/octo-release/)

[Download the native demo.](https://douglasdwyer.github.io/octo-release/octo.exe)

[See YouTube for gameplay and technical videos.](https://www.youtube.com/@DouglasDwyer?sub_confirmation=1)

This is the repository for releases of the Octo voxel game engine. The engine is designed to support the processing, modification, and rendering of large-scale voxel volumes consisting of various colors and materials. Ultimately, the goal of Octo is to become an online multiplayer platform in which users can create, interact, and extend with mods or plugins. Using voxel ray marching with compute shaders, the engine seeks to support a wide range of hardware, including integrated GPUs. Specifically, the Octo engine seeks to:

- Run at playable speeds on integrated hardware
- Run at playable speeds in a web browser
- Run at high-quality speeds on desktop with a discrete GPU

The engine is written in Rust, and runs on native platforms and the web using WASM and WebGPU.

### Supported platforms

- Native: Windows
- Web: Windows or Mac with Chrome, Edge, or Opera (or any other browser with WebGPU enabled)

### Controls

- Mouse: look around
- T: lock/unlock cursor
- G: swap material
- Left click: destroy
- Right click: build

### Features

The following features are included in the demo:

- Large-scale voxel rendering using ray marching and LODs
- Realtime path-traced lighting (ambient occlusion, shadows, and emissive voxels)
- Importing voxel models at various scales
- Fully editable voxel terrain
- TCP networked multiplayer (desktop only)

### To be re-added

The following features used to exist, but have been removed as a part of the ray marching rewrite.
They will be added back soon:

- Transparent voxel objects
- Octree-accelerated rigidbody collision detection
- Octree-accelerated terrain generation with Perlin noise
- Peer-to-peer networked multiplayer (web and desktop)

### Future plans

In the future, development is planned for the following parts of the engine:

- Immersive character and camera controls
- 3D spatial audio
- A material system that allows assigning properties to voxel types, such as textures, sound effects, and physics data
- An easy-to-use and secure modding system build on WASM plugins

### Changelog

- 0.1.1: Fixed a chunk meshing bug that was causing slower cached meshing times. World editing should now feel faster and smoother. In addition, improved left-click/right-click controls.
- 0.1.2: Fixed a chunk generation priority bug that could lead to chunks being slow to load around the player. In addition, increased voxel placement/destruction radius.
- 0.2.0: Rewrote the engine on top of the new Geese event system. Switched to greedy meshing with LODs for voxel rendering. Added snow and the ability to import voxel models.
- 0.3.0: Created a rigidbody physics system with connected component detection, collision detection, and collision response. Enabled multiplayer for the live demo. Fixed various bugs.
- 0.3.1: Added task-level and data-level multithreading, alongside other optimizations for the physics engine. Fixed various bugs.
- 0.3.2: Overhauled the networking systems related to chunk/entity synchronization. Drastically reduced network bandwidth consumption, improving multiplayer performance.
- 0.3.3: Fixed a critical issue with network chunk synchronization.
- 0.5.0: Removed all voxel-related code from the engine. Implemented new voxel data structures with ray marched graphics.
- 0.6.0: Major improvements to ray marcher performance. In addition, added back world editing, LODs, and some multiplayer functionality.
- 0.7.0: Added path-traced indirect lighting, including ambient occlusion and emissive voxels.
- 0.7.1: Upgraded winit to fix bug with mouse input on web.