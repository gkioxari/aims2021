# Lab 1: Deform Source Mesh to Target Mesh

In this practical session, we will familiarize ourselves with 3D data structures and differentiable 3D operators. The goal of this lab is to learn how to deform an initial mesh to a target shape. We will be following this PyTorch3D [tutorial][py3dlab].

## Prerequisites
* [Colab][colab]: Throughout this lab we will use colab notebooks to run the labs. This is essential as the models will run much faster on the colab GPU compared to your personal laptops (which only have CPU). 

## Instructions
Please upload your short report in the form of `firstname_lastname.pdf` (e.g. `georgia_gkioxari.pdf`) to this [dropbox link][dropbox] by Sunday, April 18. The length of the report should not exceed 2 pages and it should address the questions answered below.

## Part A: 3D Operators

In the [tutorial][py3dlab], you are asked to deform the vertices of an initial sphere mesh to fit a target shape. The loss function is `loss = loss_chamfer * w_chamfer + loss_edge * w_edge + loss_normal * w_normal + loss_laplacian * w_laplacian`

1. Describe what each loss term does with a couple of sentences for each loss term. What is the purpose of each loss term?
2. What happens if you set all weights to 0.0 **except for the chamfer weight** (`w_chamfer`)? Discuss the quality of the predicted shape and the convergence rate.
3. What happens if you set `w_edge` to 100.0? Discuss the quality of the predicted shape and the convergence rate.

## Part B: 3D Data Structures

The mesh you deform in the tutorial is an ico-4 sphere (`src_mesh = ico_sphere(4, device)`). 

1. How many vertices and how many faces does `src_mesh` have?
2. What happens if you set the level of the sphere to be 1, i.e. `src_mesh = ico_sphere(1, device)`. Discuss the quality of the predicted shape and the convergence rate.

### Helpful material

This short video [lecture][lecture] might be of help.


[dropbox]: https://www.dropbox.com/request/3gmpDzDe8Rzd11sPzKwl
[py3d]: https://github.com/facebookresearch/pytorch3d
[py3dtut]: https://github.com/facebookresearch/pytorch3d/tree/master/docs/tutorials
[py3dlab]: https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/deform_source_mesh_to_target_mesh.ipynb
[colab]: https://colab.research.google.com/
[lecture]: https://www.youtube.com/watch?v=MOBAJb5nJRI&t=8189s