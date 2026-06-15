# cobot-atlas — 3D Mesh Generation for Robot Simulation

A comprehensive collection of tools, manifests, and generated 3D mesh assets for collaborative robot (cobot) simulation environments. Meshes are generated via [fal.ai](https://fal.ai) APIs using text-to-image and image-to-mesh pipelines.

## Repository Structure

```
cobot-atlas/
├── docs/                    # Documentation
│   ├── README.md            # This file
│   └── PROMPTS_REFERENCE.md # Detailed prompt reference for all meshes
├── scripts/                 # Mesh generation & management tools
│   ├── generate_meshes.py           # Main mesh generator
│   ├── generate_meshes_parallel.py  # Parallel batch generation
│   ├── generate_meshes_robust.py    # Robust generation with retry logic
│   ├── generate_meshes_supplement.py# Supplemental generation
│   ├── batch_submit.py              # Batch submission
│   ├── batch_submit_v2.py           # Batch submission v2
│   ├── parallel_spawn.py            # Parallel spawn orchestrator
│   ├── parallel_spawn_industrial.py # Industrial environment spawn
│   ├── parallel_spawn_vla.py        # VLA environment spawn
│   ├── create_industrial_manifest.py# Industrial manifest builder
│   ├── check_progress.py            # Progress monitoring
│   ├── verify_and_document.py       # Verification & documentation
│   ├── extend_industrial_queue.py   # Extend industrial queue
│   ├── monitor_progress.sh          # Shell progress monitor
│   └── launch_swarm.sh              # Swarm launch script
├── manifests/               # Mesh definition manifests
│   ├── mesh_manifest.json                  # Core 23-mesh manifest
│   ├── mesh_manifest_1000.json             # 1000-mesh scale manifest
│   ├── mesh_manifest_combined.json         # Combined manifest
│   ├── mesh_manifest_industrial.json       # Industrial environment meshes
│   ├── mesh_manifest_vla_new.json          # VLA meshes
│   ├── mesh_manifest_supplement.json       # Supplemental meshes
│   ├── mesh_manifest_robotics_expanded.json# Expanded robotics meshes
│   └── mesh_queue_supplement.json          # Supplemental queue
└── outputs/                 # Generated mesh assets
    ├── general/             # Core 23 meshes (pick-and-place, stacking, benchmarks)
    ├── industrial/          # Industrial environment meshes
    ├── robotics/            # Robotics meshes
    ├── parallel/            # Parallel-generated meshes
    ├── parallel_supplement/ # Parallel supplement meshes
    ├── vla_new/             # VLA environment meshes
    └── batch/               # Batch-generated meshes
```

## Quick Start

```bash
# 1. Place fal.ai API keys in a file (one per line)
nano ~/.config/cobatlas/fal_api_keys.txt

# 2. Generate meshes
python scripts/generate_meshes.py --keys-file ~/.config/cobatlas/fal_api_keys.txt

# 3. Find generated meshes in outputs/<category>/<mesh_id>/
```

### Generation Methods

**Image-to-Mesh (default, recommended):** Two-step pipeline — generates a reference image via Flux then converts to 3D mesh via TripoSR. Produces higher quality results.

**Text-to-Mesh (direct):** Single API call, faster and cheaper but lower quality.

```bash
python scripts/generate_meshes.py --method image_to_mesh
python scripts/generate_meshes.py --method text_to_mesh
```

### Selective Generation

```bash
# Generate specific meshes only
python scripts/generate_meshes.py --only "red_cube,blue_cylinder,ycb_mustard"

# Skip certain meshes
python scripts/generate_meshes.py --skip "tabletop_scene,franka_panda_gripper"

# Preview without API calls
python scripts/generate_meshes.py --dry-run
```

## Mesh Manifests

Each manifest defines mesh properties:

| Field | Description |
|-------|-------------|
| `id` | Unique identifier (used as filename) |
| `category` | Type: manipulation_object, target_surface, ycb_object, etc. |
| `dimensions` | Physical size for physics proxy |
| `physics_proxy` | Collision shape: cuboid, cylinder, ball, convex_hull, trimesh |
| `mass_kg` | Mass for physics simulation |
| `material` | Material type for rendering hints |
| `purpose` | Experiment or use case |
| `text_prompt` | Prompt for text-to-mesh generation |
| `image_prompt` | Prompt for image generation step |

## Output Format

Each generated mesh has its own subdirectory with:

```
outputs/<category>/<mesh_id>/
├── <mesh_id>.glb           # 3D mesh (GLB format)
└── <mesh_id>_reference.png # Reference image (image-to-mesh only)
```

## Recovery

The generator saves progress after each mesh. To resume:

```bash
# Check progress
cat outputs/<category>/generation_log.json | jq '.jobs[] | select(.status == "completed") | .mesh_id'

# Re-run, skipping completed meshes
python scripts/generate_meshes.py --skip "red_cube,blue_cube"
```

## License

MIT License.
