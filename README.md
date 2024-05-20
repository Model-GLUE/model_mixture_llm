# Model-GLUE: Democratized LLM Scaling for A Large Model Zoo in the Wild

Code for the mixture bench of "**Model-GLUE: Democratized LLM Scaling for A Large Model Zoo in the Wild**".

## Setup

1. Setup environment
```shell
conda create -n modelglue python=3.10
conda activate modelglue

pip install -r requirements.txt
```
2. Install mergekit
```shell
git clone https://github.com/arcee-ai/mergekit.git -b mixtral
cd mergekit

pip install -e . 
```

3. Install lm-eval
```shell
git clone -b offset_by_id https://github.com/s1ghhh/lm-evaluation-harness.git
cd lm-evaluation-harness
pip install --editable ./
```
4. Install bigcode-eval
```shell
git clone https://github.com/bigcode-project/bigcode-evaluation-harness.git
cd bigcode-evaluation-harness && git checkout 00967d1
pip install --editable ./
```

## Model Mixture 
```shell
. scripts/run_mixture.sh
```

## Evalution
Please refer to `eval_tools.py`