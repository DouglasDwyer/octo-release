# Octo Project

[Try the online demo now.](https://douglasdwyer.github.io/octo-release/)

[See YouTube for gameplay and technical videos.](https://www.youtube.com/channel/UCjVn35Ubo5c2wagQ6bgVT1Q)

This is the repository for releases of the Octo voxel game engine. The engine is designed to support the processing, modification, and rendering of large-scale voxel volumes consisting of various materials. Ultimately, the goal of Octo is to become an online multiplayer platform in which users can create, interact, and extend with mods or plugins. Using a rasterization/ray marching hybrid technique, the engine seeks to support a wide range of hardware, including integrated GPUs. Specifically, the Octo engine seeks to:

- Run at playable speeds on integrated hardware
- Run at playable speeds in a web browser
- Run at high-quality speeds on desktop with a discrete GPU

The engine is written in Rust, and runs on the web using WASM and WebGL 2.0. A native version of the game will be offered in the future.

### Controls

- Mouse: look around
- T: lock/unlock cursor
- Left click: destroy
- Right click: build

### Features

The follow features are included in the demo:

- Large-scale voxel rendering using parallax ray marching
- Realtime diffuse/specular lighting with directional shadows
- Fully editable voxel terrain
- Octree-accelerated terrain generation with Perlin noise

### Future plans

In the future, development is planned for the following parts of the engine:

- Support for transparent voxel objects
- Lighting with shadows for multiple light sources
- Rigidbody-based physics engine
- An easy-to-use and secure modding system build on WASM plugins
- Multiplayer - already implemented with WebRTC, but disbaled for this demo

### Changelog

- 0.1.1: Fixed a chunk meshing bug that was causing slower cached meshing times. World editing should now feel faster and smoother. In addition, improved left-click/right-click controls.