# Lab 1: Deform Source Mesh to Target Mesh

In this lab session, we will familiarize ourselves with 3D data structures and differentiable 3D operators. 
In this exercise, we will learn how to deform an initial 3D mesh shape (e.g. sphere) to a target 3D mesh shape (e.g. dolphin). 
We will be following the PyTorch3D [tutorial][py3dlab].

## Prerequisites
* [Colab][colab]: We will use colab notebooks to run the tutorials. This is essential as the models will run much faster on the colab GPU compared to your personal laptops (which only have CPU). 
To run PyTorch3D tutorials on colab, follow the [instructions][py3dinstr]. First, you'll need to enable GPUs for the notebook: Navigate to Edit --> Notebook Settings and select GPU from the Hardware Accelerator drop-down.
To verify you are running on a GPU, run `torch.cuda.is_available()`.

## Instructions
Please upload your short report in the form of `firstname_lastname.pdf` (e.g. `georgia_gkioxari.pdf`) to this [dropbox link][dropbox] by Sunday, April 18. The length of the report should not exceed 2 pages and it should address the questions answered below.

## Part A: 3D Operators

In the [tutorial][py3dlab], you are asked to deform the vertices of an initial sphere mesh to fit a target shape.

1. The objective is comprised of a set of loss functions with associated weights. Describe what the purpose of each loss is in a couple of sentences per loss term.
2. What happens if you set all loss weights to 0.0 **except for the chamfer weight** (`w_chamfer`)? Discuss the quality of the predicted shape and the convergence rate.
3. What happens if you set `w_edge` to 100.0? Discuss the quality of the predicted shape and the convergence rate.

## Part B: 3D Data Structures

The initial sphere mesh, which you deform in the tutorial, is an `ico-4` sphere (`src_mesh = ico_sphere(4, device)`). 

1. How many vertices and how many faces does `src_mesh` have?
2. What happens if you set the level of the sphere to be 1, i.e. `src_mesh = ico_sphere(1, device)`. How many vertices and faces does the shape have now? Discuss the quality of the predicted shape and the convergence rate when you initialize the shape with an `ico-1` sphere.

## Helpful material

This short [video lecture][lecture] will be of help.


[dropbox]: https://www.dropbox.com/request/3gmpDzDe8Rzd11sPzKwl
[py3d]: https://github.com/facebookresearch/pytorch3d
[py3dtut]: https://github.com/facebookresearch/pytorch3d/tree/master/docs/tutorials
[py3dlab]: https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/deform_source_mesh_to_target_mesh.ipynb
[colab]: https://colab.research.google.com/
[lecture]: https://youtu.be/MOBAJb5nJRI?t=1724
[py3dinstr]: https://pytorch3d.org/tutorials/