# Pretrained Models

Download the released checkpoints from Google Drive and place them directly in
this folder:

- Google Drive: [3dpr pretrained checkpoints](https://drive.google.com/drive/folders/1KdS9KlDL70JpSAZilIoyyGZU5-UXwA-l?usp=sharing)

Expected layout:

```text
pretrained_models/
|-- ffhqrebalanced512-128.pkl
|-- encoder_FFHQ.pt
|-- afa_FFHQ.pt
`-- network-snapshot-000225.pkl
```

Expected files:

- `ffhqrebalanced512-128.pkl`: pretrained 3D generator checkpoint used as
  `G_CKPT`.
- `encoder_FFHQ.pt`: inversion encoder checkpoint used as `E_CKPT`.
- `afa_FFHQ.pt`: AFA checkpoint used as `AFA_CKPT`.
- `network-snapshot-000225.pkl`: released reflectance / relighting checkpoint
  used by [`scripts/inference_relighting.sh`](../scripts/inference_relighting.sh)
  as the default `R_CKPT`.

You can override these defaults with `G_CKPT`, `E_CKPT`, `AFA_CKPT`, or
`R_CKPT` when running the inference wrapper.
