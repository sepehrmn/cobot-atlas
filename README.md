# cobot-atlas

**A large-scale 3D mesh dataset for robot simulation, manipulation research, and embodied AI.**

cobot-atlas provides 2,023 unique 3D meshes (glTF 2.0 Binary) spanning industrial components, geometric primitives, household items, YCB benchmark objects, robot hardware, and more — designed for collaborative robot simulation, VLA model training, and robotics benchmarking.

## Dataset

The full dataset is hosted on Hugging Face:

**[torusprime/cobot-atlas](https://huggingface.co/datasets/torusprime/cobot-atlas)** — 2,024 GLB files, 33.5 GB, MIT license.

| Category | Count | Examples |
|----------|------:|----------|
| Industrial | 734 | ICs, connectors, bearings, gears, motors, sensors, fasteners |
| Primitives | 228 | Cubes, spheres, cylinders, cones, tori in various colors |
| Household | 179 | Kitchen utensils, containers, bottles, furniture |
| Manipulation | 163 | Stacking blocks, peg-in-hole, Hanoi tower, shape sorters |
| Robotics | 88 | Robot arms, grippers, depth cameras, mobile bases |
| YCB Objects | 72 | Mustard bottle, spam can, cracker box, bowls, cups |
| Food | 66 | Fruits, vegetables, prepared items |
| + 24 more | 493 | Fabric, tools, toys, vehicles, lab equipment, medical, art supplies |
| **Total** | **2,024** | |

## This Repository

This repo contains the **generation pipeline** — scripts, manifests, and tools used to produce the dataset.

```
scripts/       — Mesh generation (fal.ai text-to-image → image-to-3D)
manifests/     — Item definitions with prompts (10 manifest files)
outputs/       — Generated meshes (GLB + reference PNG + metadata)
docs/          — Documentation and prompt reference
```

### Usage

```bash
pip install fal-client requests

# Generate meshes from manifests
python scripts/generate_meshes.py

# Verify outputs against manifests
python scripts/verify_and_document.py
```

## Sister Project

**[relief-atlas](https://github.com/sepehrmn/relief-atlas)** — 10,000+ meshes for disaster relief, humanitarian aid, and civil protection (Germany DRK/THW/Feuerwehr, EU Civil Protection, Ukraine recovery, global disaster response).

## Citation

If you use cobot-atlas in your research, please cite:

```bibtex
@dataset{cobot_atlas_2026,
  author    = {Mahmoudian, Sepehr},
  title     = {cobot-atlas: A Large-Scale 3D Mesh Dataset for Robot Simulation},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.20697491},
  url       = {https://doi.org/10.5281/zenodo.20697491}
}
```

## License

MIT
