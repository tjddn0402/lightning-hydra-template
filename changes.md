# `lightning.pytorch` -> `pytorch_lightning`
```bash
find . -type f -exec sed -i 's/lightning.pytorch/pytorch_lightning/g' {} +
```

# .vscode/launch.json 
```JSON
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python: Current File",
            "type": "python",
            "request": "launch",
            "program": "${file}",
            "console": "integratedTerminal",
            "justMyCode": true,
            "cwd": "${fileDirname}"
        }
    ]
}
```

# how to run
0. 이 repo clone 하고 install
```bash
git clone https://github.com/tjddn0402/lightning-hydra-template.git
pip install -e .
```
1. train
```bash
python train.py
```
1. `eval.yaml` 수정
```bash
ckpt_path: /path/to/checkpoint.ckpt
```
1. eval
```bash
python eval.py
```