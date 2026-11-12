# Changelog - Low-Poly Toy Cars

## 2026-11-12 fix - no more flickering faces
- Fixed z-fighting: where two differently coloured surfaces shared the same plane (decals, labels, trims, prints, inner parts) they flickered in and out as the camera moved. They now sit at least 2 mm apart. File names, sizes, pivots, rigs, animations, materials and textures are unchanged; vertices moved by a few millimetres at most.

## v3.0 - November 2026 (free update for everyone who owns the pack)

The pack grows from 20 to 50 vehicles. I added 30 new ones, and the original 20 did not change.

**30 new vehicles, 3 colourways each (90 new files per format)**
- City: ambulance, city bus, school bus, garbage truck, delivery (step) van, double-decker bus, tuk-tuk, street sweeper, SUV
- Work: tractor, cement mixer, dump truck, digger (backhoe loader), forklift (with pallet and crate), crane truck, road roller, tanker truck
- Fun: kart, camper van (pop-top), limousine, mini car, motorbike, scooter, supercar, quad bike, golf cart
- Extras: toy tank (no insignia), toy plane on wheels (with a spinning propeller node), tiny train engine, six-wheeled space rover

**What stays the same**
- Vehicles 01-20 are byte-identical to v2: same file names, node names, scale and pivots. Your existing scenes and code keep working.
- The same rules as before: wheels are separate nodes, the origin is at the wheel centre and the spin axis is local X. Each file has one palette material, and the scale is 1 unit = 1 m with front = +Z.

**New in v3**
- Glowing lights: vehicles 21-50 have an emissive map in the GLB for head lights, tail lights and amber/blue beacons. The FBX files have no emission, because Blender's FBX exporter puts the whole palette into that slot. The emissive PNG ships next to the files.
- More wheel layouts: 3 axles (wheel_ML / wheel_MR), centre wheels for the bikes, tuk-tuk, road roller drum and plane tail wheel, and a `propeller` node on the plane.
- The palette PNGs (base colour, metal/roughness, emissive) now ship next to every file in both zips. The v2 README said they were included, but they were not.
- vehicles.csv (replaces cars.csv) and manifest.json list every file with its triangles, size, category and wheel node names.
- 2,976 to 8,750 triangles per vehicle across the whole pack (average 5.7k). The 20 v2 cars are still 4,072 to 7,804.

**Checked**
- Khronos glTF-Validator: 0 errors, 0 warnings on all 150 GLB files.
- All 90 new FBX files re-imported in Blender with the embedded texture found. No build-machine paths are left in any FBX.
- Wheel pivots, ground contact and wheel-to-body clipping were checked by script on all 50 vehicles.

## v2 - October 2026
All 20 cars were rebuilt with chamfered bodies, proper wheel arches, real rims and tyres, and 3 colourways each.

## v1
First release: 20 toy cars.
