# Multi Lab

## Overview

Multi Lab is a public template for artificial intelligence and machine learning research projects using Lightning AI's [PyTorch Lightning](https://lightning.ai/docs/pytorch/latest/).

The recommended way for Multi Lab users to create new repos is with the [use this template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template) button.

An adaptation can be found at [lightning-vision](https://github.com/JustinGoheen/multilab-vision).

## Source Module

`multilab.core` should contain code for the Lightning Module and Trainer.

`multilab.components` should contain experiment utilities grouped by purpose for cohesion.

`multilab.pipeline` should contain code for data acquistion and preprocessing, and building a TorchDataset and LightningDataModule.

`multilab.serve` should contain code for model serving APIs built with [FastAPI](https://fastapi.tiangolo.com/project-generation/#machine-learning-models-with-spacy-and-fastapi).

`multilab.cli` should contain code for the command line interface built with [Typer](https://typer.tiangolo.com/)and [Rich](https://rich.readthedocs.io/en/stable/).

`multilab.pages` should contain code for data apps built with streamlit, dash, or reflex. the `pages` module naming convention is borrowed from React concepts.

`multilab.config` can assist with project, trainer, and sweep configurations.

## Base Requirements and Extras

Multi Lab installs requirements out of the box, and provides extras to make creating robust virtual environments easier. To view the requirements, in [setup.cfg](setup.cfg), see `install_requires` for the base requirements and `options.extras_require` for the available extras.

The recommended install is as follows:

```sh
python3 -m venv .venv
source .venv/bin/activate
pip install -e ".[all]"
```
