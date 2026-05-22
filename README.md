# NetworkVR

A virtual reality application built in Unity for immersive 3D network visualization and exploration.

NetworkVR allows users to explore graph and network datasets spatially in VR. Nodes and edges are rendered in a fully interactive 3D environment, making it easier to investigate relationships, clusters, and structures that may be difficult to interpret in traditional 2D visualizations.

The project was developed in Unity using C#, OpenXR, and the XR Interaction Toolkit.

---

# Features

- Immersive 3D network visualization in VR
- Dynamic edge rendering with intermediate path points
- Multiple preloaded example datasets
- VR locomotion and navigation
- Network search system
- Spatial exploration of complex graph structures
- Interactive node label toggling using VR controllers

---

# Included Networks

The current version of the project contains three built-in example networks:

## 1. Zachary's Karate Club

A social network dataset representing friendships between members of a university karate club.

---

## 2. University Network

A network visualization of universities and their relationships.

(More information coming soon.)

---

## 3. UVA Faculty Network

A visualization of UVA faculty members and their associated academic fields.

---

# Current Status

At the moment, users cannot yet upload their own datasets directly through the application.

Custom network importing is planned for a future update.

---

# Requirements

## Software

- Unity 2022.3 LTS (recommended)
- OpenXR-compatible VR headset

## Unity Packages

This project uses:

- Pcx Point Cloud Renderer: https://github.com/keijiro/pcx
- XR Interaction Toolkit
- OpenXR Plugin
- Input System
- TextMeshPro
- XR Core Utilities

---

# Supported Hardware

Designed for PC VR headsets including:

- Meta Quest 2 / Quest 3 (via Link)
- Valve Index
- HTC Vive
- Other OpenXR-compatible headsets

---

# Installation

## 1. Clone the Repository

```bash
git clone https://github.com/isabelxiao1/NetworkVR.git
```
---

## 2. Open the Project

1. Open Unity Hub
2. Click "Add Project"
3. Select the cloned `NetworkVR` folder
4. Open using the recommended Unity version

---

# Running the Project

1. Connect and enable your VR headset
2. Launch SteamVR or Meta Quest Link (if applicable)
3. Open the project in Unity
4. Open the main scene
5. Press Play

---

# Controls

| Action | Control |
|---|---|
| Move | Left joystick |
| Turn | Right joystick |
| Toggle menu | Right lower trigger |
| Interact / Select nodes | Main trigger |
| Toggle node labels | Click on nodes |
| Zoom movement | Right A button |

---

# Network Data Format

Future versions of the project will support custom network uploads.

The application uses two CSV files:

- Nodes CSV
- Edges CSV

---

## Nodes CSV Format

Required columns:

| Column | Description |
|---|---|
| id | Unique node identifier |
| x | X position |
| y | Y position |
| z | Z position |
| colors | Node color |
| size | Node size |
| label | Node label text |

Example:

```csv
id,x,y,z,colors,size,label
1,0,0,0,#FF0000,1.5,NodeA
2,1,2,0,#00FF00,1.0,NodeB
```

---

## Edges CSV Format

Required columns:

| Column | Description |
|---|---|
| source | Source node ID |
| target | Target node ID |
| path | Intermediate edge path positions |
| colors | Edge color |

- `source` and `target` reference node IDs from the nodes CSV.
- `path` is a list of numbers where every 3 numbers represent the XYZ coordinates of an intermediate point along the edge.

Example:

```csv
source,target,path,colors
1,2,0.5;0.2,0.0;0.7;0.8;0.1,#FFFFFF
```

# Future Improvements

- User-uploaded network support
- Larger dataset optimization
- Improved edge rendering
- Additional interaction systems

---

# License

MIT License

---

# Author

Created by Isabel Xiao :)
- Statistics @ UVA
- Connected Data Hub @ UVA SDS
