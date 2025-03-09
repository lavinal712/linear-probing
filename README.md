# Linear Probing

This repository contains a simple implementation of linear probing for CLIP models. To evaluate CLIP-ViT-L/14, run:

```bash
python main.py \
    --batch_size 512 \
    --model openai/clip-vit-large-patch14 \
    --embed_dim 1024 \
    --epochs 90 \
    --blr 0.1 \
    --weight_decay 0.0 \
    --dist_eval \
    --data_path /path/to/ImageNet \
```

The code can be simply modified to evaluate other models with few code changes.

## Evaluation

The evaluation is done on the ImageNet-1K. The results are as follows:

| Model         | Top-1 Accuracy | Top-5 Accuracy | Batch Size | Seed |
|---------------|----------------|----------------|------------|------|
| CLIP-ViT-L/14 | 83.9           | -              | 512        | 0    |


## Acknowledgements

Thanks to the following projects:

- [MAE](https://github.com/facebookresearch/mae)
- [DINO](https://github.com/facebookresearch/dino)
