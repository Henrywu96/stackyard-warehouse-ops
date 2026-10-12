# Stackyard Warehouse Ops

A 3D warehouse control room that runs in the browser. A simulated distribution center (DC-02 Northgate) keeps working while you watch: AGV forklifts put away inbound pallets, pick orders, stage them at the dock doors and recharge when their batteries run low.

All data is simulated. Nothing connects to a real warehouse system.

## What you can do

- **Watch the floor:** 144 pallet positions across blue racks, four AGVs, inbound lanes and dock doors, rendered in 3D.
- **Track the shift:** live figures across the top for bin utilization, pallets on hand, shipped and received today, and open tasks.
- **Follow the fleet:** the left panel lists each AGV with its battery and current job, the task queue and an activity log.
- **Inspect anything:** click a rack position to see the pallet stored there in the inspector on the right, or click an AGV to follow it with the camera.
- **Find stock:** search by SKU or product name and the camera flies to the oldest pallet on hand (first in, first out).
- **Recolor the racks:** color pallets by category, velocity (how fast they move) or age.
- **Drive the simulation:** pause, run at ×1, ×2 or ×4, toggle automatic orders, place a new order or receive a truck.
- **Jump around:** click the floor plan in the corner to move the camera.

## Controls

| Action | Input |
| --- | --- |
| Orbit · pan · zoom | Drag · right-drag · scroll |
| Inspect a rack position or AGV | Click it |
| Follow the selected AGV | `F` |
| Iso view · top view | `1` · `2` |
| Pause or resume | `Space` |
| Search | `/` |
| Clear selection | `Esc` |

## Run it locally

No build step. Because the page loads ES modules, open it through a local server rather than double-clicking the file:

```bash
npx serve .
# or
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Built with

- [three.js](https://threejs.org/) 0.160, loaded from the jsDelivr CDN (3D scene, orbit controls)
- Big Shoulders Display, IBM Plex Sans and IBM Plex Mono from Google Fonts
- Plain HTML, CSS and JavaScript in a single `index.html`; every model is built in code
