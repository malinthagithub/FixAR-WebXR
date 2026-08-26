# FixAR

## A Web-Based AR Equipment Familiarisation and Guided Visual Inspection Trainer

FixAR is a browser-based WebXR application developed to help trainees familiarise themselves with industrial equipment and practise a basic guided visual inspection sequence before interacting with real equipment.

The application combines marker-based AR and markerless WebXR in a mobile-friendly web experience.

---

## Main Features

### 1. Marker-Based AR Equipment Preview
- Uses AR.js and A-Frame
- Detects a Hiro marker
- Displays industrial 3D equipment
- Allows the user to switch between:
  - Conveyor System
  - Industrial Water Pump

### 2. Markerless WebXR Training
- Uses Three.js and WebXR
- Detects suitable real-world surfaces
- Places equipment using WebXR hit-testing
- Supports:
  - Rotate Left / Right
  - Increase / Decrease Size
  - Move / Reposition
  - Remove
  - Restart

### 3. Guided Visual Inspection Training
The user can start a guided inspection for the selected equipment.

The system:
- focuses on one equipment model
- highlights one inspection area at a time
- provides inspection instructions
- allows rotation and resizing during inspection
- guides the user through four inspection stages
- records completion of each inspection checkpoint

This feature is intended for equipment familiarisation and training only. It does not replace formal workplace inspection procedures, qualified supervision, or safety procedures.

---

## Equipment

### Conveyor System
Guided inspection areas:
1. Conveyor Frame
2. Belt / Carrying Surface
3. Drive / Pulley Area
4. Base / Supports

### Industrial Water Pump
Guided inspection areas:
1. Pump Housing
2. Inlet / Outlet Connections
3. Electric Motor Housing
4. Base / Mounting

---

## Technologies Used

- HTML5
- CSS3
- JavaScript
- Three.js
- WebXR Device API
- WebXR Hit Test
- AR.js
- A-Frame
- GLTF / GLB 3D models
- GitHub Pages

---

## Advanced Interaction

The markerless AR experience implements a multi-step interaction flow:

Select Equipment  
→ Detect Surface  
→ Place Equipment  
→ Rotate / Resize  
→ Reposition  
→ Start Inspection  
→ Review Sequential Inspection Areas  
→ Complete Training

This requires interaction state management for equipment selection, placement, repositioning, manipulation, guided inspection, and completion.

---

## Browser and Device Testing

The markerless WebXR experience was primarily tested using Google Chrome on an Android smartphone.

Surface detection was found to work best on well-lit surfaces with visible visual features or texture.

Standard iOS browsers do not currently provide the same immersive WebXR functionality required by the markerless training experience.

---

## 3D Model Performance

- Conveyor model: approximately 38 KB
- Water Pump model: approximately 10.9 MB

The models were selected to provide an appropriate balance between mobile performance and visual quality.

---

## Project Structure

```text
FixAR-WebXR/
│
├── index.html
├── marker.html
├── training-ar.html
├── css/
│   └── style.css
├── models/
│   ├── conveyor.glb
│   └── machine.glb
└── README.md
