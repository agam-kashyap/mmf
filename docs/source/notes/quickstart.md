# Quickstart [![](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Z9fsh10rFtgWe4uy8nvU4mQmqdokdIRR) [![](https://circleci.com/gh/facebookresearch/mmf.svg?style=svg)](https://circleci.com/gh/facebookresearch/mmf)

**Authors**: Amanpreet Singh

In this quickstart, we are going to train M4C model on TextVQA. Follow instructions at the bottom
to train other models in MMF.

## Demo

1. [VQA](https://colab.research.google.com/drive/1Z9fsh10rFtgWe4uy8nvU4mQmqdokdIRR)
2. [Captioning](https://colab.research.google.com/drive/1vzrxDYB0vxtuUy8KCaGxm--nDCJvyBSg)

## Citation

If you use MMF in your work, please cite:

[Add new citation]

## Installation

Install MMF using pip

```
pip install --upgrade --pre mmf
```

```eval_rst
.. note::

  1. For more details about installation check the [Installation documentation](./installation).
  2. You can also create/activate your own conda environments before running
     above commands.
```

## Getting Data

In MMF datasets and required files will be downloaded automatically when we run training next. For more details about custom datasets and other advanced setups for datasets check the [Dataset documentation](../tutorials/concepts).

## Training

Now we can start training by running the following command:

```
mmf_run config=projects/m4c/configs/textvqa/defaults.yaml datasets=textvqa model=m4c run_type=train_val
```

## Inference

For running inference or generating predictions, we can specify a pretrained model using it's zoo key and then run the following command:

```
mmf_predict config=projects/m4c/configs/textvqa/defaults.yaml datasets=textvqa model=m4c run_type=test checkpoint.resume_zoo=m4c.textvqa.defaults
```

For running inference on `val` set, use `run_type=val` and rest of the arguments remain same. Check more details in [pretrained models](pretrained_models) section.

These commands should be enough to get you started with training and performing inference using MMF.

## Next steps

To dive deep into world of MMF, you can move on the following next topics:

- [Concepts and Terminology](../tutorials/concepts)
- [Using Pretrained Models](./pretrained_models)
- [Challenge Participation](./challenge)
