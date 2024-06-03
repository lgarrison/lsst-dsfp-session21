# LSST DSFP Session 21: Lectures & Problem Sets IX & X

## Author
[Lehman Garrison](https://github.com/lgarrison)\
Research Software Engineer\
[Scientific Computing Core](https://www.simonsfoundation.org/flatiron/scientific-computing-core/)\
[Flatiron Institute](flatironinstitute.org)

## Overview
This repo contains lectures and problem sets from [LSST DSFP Session 21](https://github.com/bscot/Session21-planning) classes IX and X on "High-Performance Python and Parallelization" and "GPU-Accelerated Python". The materials cover a bit of NumPy, Numba, CPU parallelism with Numba, CuPy, and CUDA with Numba. The notebooks should take roughly 1–1.5 hours each to go through. They assume a little bit of Python and NumPy background and reference some concepts from astronomy, but don't assume any experience with compiled languages (including the CUDA sections, where we stick with Python).

## How to run these notebooks
### Option 1: Google Colab
This is the easiest option, unless you want to experiment with the parallelization material in Lecture/Problem Set IX (the free tier of Google Colab only offers 1 physical CPU core).

| Notebook | Link |
|----------|------|
| Lecture IX: High-Performance Python: NumPy, Numba, and Parallel Numba | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lgarrison/lsst-dsfp-session21/blob/main/lecture_ix.ipynb) |
| Problem Set IX: Let's Write a 2PCF Code! | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lgarrison/lsst-dsfp-session21/blob/main/problem_ix.ipynb) |
| Lecture X: GPU-Accelerated Python with CuPy and Numba | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lgarrison/lsst-dsfp-session21/blob/main/lecture_x.ipynb) |
| Problem Set X: Practicing GPU-Accelerated Python | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lgarrison/lsst-dsfp-session21/blob/main/problem_x.ipynb) |

To run GPU code, you'll need to specifically select the runtime type in Colab:
- Select the arrow next to "Connect" in the top right
- Select "Change runtime type"
- Choose a GPU (the T4 should be plenty for these notebooks)
- Click Save


### Option 2: Flatiron Institute BinderHub
Flatiron Institute hosts a public BinderHub that allows several CPUs per user, as well as a small GPU slice. This is a good option for working on CPU parallel code, or as an alternative to Colab GPUs. However, the service can only handle a few dozen simultaneous users.

| Environment | Link |
|-------------|------|
| CPU-only | [![Binder](https://mybinder.org/badge_logo.svg)](https://binder.flatironinstitute.org/~lgarrison/dsfp-session21)
| GPU-enabled | [![Binder](https://mybinder.org/badge_logo.svg)](https://binder.flatironinstitute.org/~lgarrison/dsfp-session21-cuda)

See here for general FI BinderHub documentation: https://wiki.flatironinstitute.org/Public/UsingFiBinder

### Option 3: Run Locally

You can also run any of these notebooks locally. You might want to follow these steps to set up a conda environment:

```console
$ git clone https://github.com/lgarrison/lsst-dsfp-session21
$ cd lsst-dsfp-session21
$ conda env create -f environment.yml -n dsfp-21
```

For Lecture and Problem Set X, you'll need an NVIDIA GPU to run the CUDA code. You can comment out all the `cu*` dependencies in `environment.yml` before creating the environment if you're not planning on using CUDA.

## License
[MIT](./LICENSE.md)
