# `lightning.pytorch` -> `pytorch_lightning`
```
find . -type f -exec sed -i 's/lightning.pytorch/pytorch_lightning/g' {} +
```
