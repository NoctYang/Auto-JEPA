# Auto-JEPA

**A Latent World Model of Continuous Intent for End-to-End Autonomous Driving**

Auto-JEPA learns a continuous future driving-intent representation through
joint-embedding prediction and grounds that representation through trajectory
retrieval and scene-conditioned candidate selection.

## Highlights

- Frozen visual encoder during driving-domain training.
- Continuous future ego-intent prediction in trajectory latent space.
- Non-parametric retrieval from a ground-truth trajectory memory.
- Scene-conditioned trajectory scoring and drivable-area feasibility filtering.
- No object boxes, occupancy labels, or surrounding-agent motion annotations.
- No learned trajectory generator.

## Results

| Benchmark | Metric | Score |
|---|---:|---:|
| NAVSIM v1 | PDMS | **91.3** |
| NAVSIM v2 | EPDMS | **89.1** |

## Repository Layout

    autojepa/
      models/       Intent predictor and trajectory representation modules
      retrieval/    Trajectory memory construction and latent retrieval
      selection/    Scene scorer and drivable-area feasibility gate
    configs/        Training and evaluation configurations
    scripts/        Training, export, and NAVSIM evaluation entry points
    assets/         Figures and lightweight documentation assets

## Status

The repository is being organized for reproducible release. Training,
retrieval, candidate selection, and NAVSIM evaluation code will be migrated
from the research workspace into the structure above.

## License

Original Auto-JEPA code is released under the [MIT License](LICENSE).
Third-party code, datasets, and model weights remain subject to their original
licenses and terms of use.
