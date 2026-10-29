# plastic-mulched-row-dataset
# PGRNet Dataset

A field image dataset for plastic-mulched row centerline detection
and vision-based agricultural navigation.

## Download

- File name: `PGRnet data set.rar`
- Baidu Netdisk: [Download dataset](https://pan.baidu.com/s/1TuTLarFurgFFhSiL5_8IhA)
- Extraction code: `msme`
- Archive format: RAR

Download and extract the archive to access the images and annotations.

## Dataset Information

| Item | Details |
|------|---------|
| Total images | 6,101 |
| Image resolution | 512 × 512 pixels |
| Image format | JPG |
| Annotation format | LabelMe JSON |
| Annotation type | Centerline polylines (`linestrip`) |
| Original manually annotated images | 3,053 |
| Automatically propagated/model-assisted annotations | 3,048 |
| Source videos | 23 |

Each image has a corresponding JSON annotation with the same filename stem.

## Annotation Method

The dataset combines original manual annotations with automatically
propagated and model-assisted annotations.

Additional frames were extracted at available half-second timestamps.
Their annotations were generated using image registration, optical flow,
and model-assisted refinement of nearby manual annotations.

## Annotation Quality

A total of 610 automatically annotated images are flagged for priority review.
Automatic annotations have not all been independently verified by human annotators.

For quantitative evaluation, manually verified annotations are recommended.

## Data Splitting

When creating training, validation, and test sets, group images by source
video or field. Keep neighboring frames from the same video in the same
split to reduce overlap between highly similar images.
