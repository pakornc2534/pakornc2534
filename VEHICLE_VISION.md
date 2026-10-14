# Vehicle Vision

**CCTV vehicle recognition deployed in Ang Sila and Don Hua Lo, Chonburi.**  
Engineering case study · Pakorn Chompunut · Updated 14 October 2026

[← Back to my profile](README.md)

![Vehicle Vision project cover](vehicle-vision.svg)

## Live deployment

Vehicle Vision is deployed in **Ang Sila (อ่างศิลา)** and **Don Hua Lo (ดอนหัวฬ่อ), Chonburi, Thailand**. My work supports the deployed system through model development, data quality, evaluation, and model updates.

## The problem

A classifier that works on one camera can struggle on another. Vehicle crops differ in size, angle, lighting, occlusion, and background. Similar brands and uncommon classes make aggregate accuracy an incomplete view of the system.

Vehicle Vision brings vehicle-brand and color recognition into a CCTV workflow. The broader project includes vehicle detection and license-plate processing. This case study focuses on my **model-team work: data preparation, classification, evaluation, and packaging for the deployment team**. The edge deployment target is NVIDIA Jetson AGX Orin.

## How the work evolved

| Stage | Engineering work |
| :--- | :--- |
| **Initial contribution** | MobileNetV3 multi-task classification, dataset and label checks, group-aware splitting, error analysis, and model artifacts for the team. The project was recognized with a Bronze Medal in Super AI Engineer Season 6. |
| **Broader camera coverage** | New CCTV crops and review workflows, duplicate screening, separation of AI observations from human labels, and investigation of tracking/identity errors. |
| **MobileNetV4 development** | Brand/color classification, controlled training recipes, checkpoint lineage, and comparisons with prior models on the same inputs. |
| **Evaluation and handoff** | Per-camera and per-class reports; packages containing model weights, configuration, class maps, and inference instructions. |
| **Current iteration** | Ongoing model improvements for the deployed system, including Formula C comparisons with v010A and other research variants. |

## A measured milestone: 20 cameras, 1,042 images

The 12 October evaluation used **1,042 available vehicle images with human-reviewed labels across 20 cameras**. Each evaluated model saw the same images. Predictions were scored at image-level top-1 without confidence filtering.

| Evaluated model | Brand correct | Brand accuracy | Color correct | Color accuracy |
| :--- | ---: | ---: | ---: | ---: |
| MobileNetV3 Large checkpoint | 508 / 1,042 | 48.75% | 797 / 1,042 | 76.49% |
| MobileNetV4 v007r1 | 847 / 1,042 | 81.29% | 920 / 1,042 | 88.29% |
| MobileNetV4 v010A | 847 / 1,042 | 81.29% | 920 / 1,042 | 88.29% |

The v010A result represents **+32.53 percentage points in brand accuracy** compared with the evaluated V3 checkpoint on this particular set. v007r1 and v010A have equal aggregate scores here, but do not make identical brand predictions: v010A corrects 15 previously wrong images and loses 15 previously correct ones.

### What makes the comparison interpretable

- The evaluated V3 has **39 brand / 8 color outputs**; these V4 variants have **37 brand / 8 color outputs**. Each checkpoint uses its own class map and preprocessing.
- Known reference classes outside a model's output vocabulary are counted as incorrect. The V4 results include one Geely image and three purple-color images outside its output heads.
- This is the available image subset: the source CSV contains 1,953 rows, while 911 referenced vehicle images are absent from this package. Separate plate images are excluded.
- Hash/pixel and near-duplicate screening found no matches under the checks performed against the available training history. Some historical files are missing, and physical-vehicle identity across crops is not fully certified. The result should not be presented as a proven, perfectly independent holdout.
- These are offline image-classification results. They do not establish live-camera accuracy, end-to-end tracking performance, or Jetson/TensorRT throughput.

## Latest development: Formula C

As of 14 October, model development includes Formula C. The latest comparison against the v010A package used the **same reused development images with AI reference labels**:

| Model | Brand accuracy · 791 known-label images | Color accuracy · 861 known-label images |
| :--- | ---: | ---: |
| v010A | 86.73% | 88.50% |
| Research baseline D | 88.24% | 88.50% |
| Formula C | **89.00%** | **89.43%** |

Formula C adds 18 correct brand predictions net versus v010A: 22 corrected, 4 regressed. Its brand result improves in nine of ten cameras in this development comparison and decreases in one.

**The tradeoff matters:** Nissan drops from 33/43 correct for v010A to 31/43 for C. Chevrolet stays at 9/16. Formula C did not pass every strict regression guard used during research. These development results do not establish independent generalization.

The development set has been used repeatedly for tuning, uses AI reference labels, and includes correlated images. These percentages should not be mixed with the human-reviewed 1,042-image evaluation above or marketed as universal accuracy.

## What the experiments taught me

**More data needs a controlled comparison.** Targeted additions improved some Suzuki cases, but the expanded-data variant did not beat its matched existing-data control overall. Gains in one class can be offset by losses elsewhere.

**Freezing the encoder has a cost as well as a benefit.** Head-only trials preserved color predictions but did not reliably repair weak-brand recall. More aggressive head updates traded some corrected vehicles for new errors in other brands.

**The review process is part of the model.** Human labels, AI observations, and prior model predictions need separate provenance. A corrected label must not quietly rewrite a frozen reference set, and development errors must not leak into training.

**Deployment is a separate validation step.** A working PyTorch/MPS evaluation and a complete model package do not prove performance on CUDA, Jetson, or TensorRT. The deployment team needs matching preprocessing and class maps, repeatable inference, and an explicit list of known regressions.

## My focus in the project

- Preparing and auditing vehicle-image datasets and label-review workflows.
- Developing and comparing brand/color classification models.
- Investigating per-camera errors, difficult classes, and regression tradeoffs.
- Preparing checkpoints, configuration, class maps, evaluation evidence, and inference instructions for the deployment team.

**Tools:** Python · PyTorch · MobileNetV3 / MobileNetV4 · NVIDIA A100 · Apple MPS · NVIDIA Jetson AGX Orin deployment target.

## Evidence behind this write-up

This public summary was checked against the local project handoff and experiment artifacts: the 12 October per-model evaluation metrics, the 14 October controlled C/K comparison and subsequent head-only experiments, and the latest deployment-handoff request. Deployment locations reflect the project owner’s update on 14 October 2026. It intentionally contains aggregate results and engineering context rather than raw CCTV data or access details.

[Discuss the engineering →](mailto:pakorn.c@ntplc.co.th) · [Back to my profile →](README.md)
