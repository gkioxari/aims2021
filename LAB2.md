# Lab 2: Differentiable Textured Rendering

In this practical session, we will explore differentiable mesh rendering. We will learn how to deform an initial sphere mesh so that it fits a set of 2D views. This lab uses the PyTorch3D [tutorial][py3dlab]. Note that just like in Lab1, we learn how to deform the vertices of an initial ico sphere. However, unlike Lab1 we don't have access to the target 3D shape. Instead, we have access to 2D views of the shape from multiple viewpoints.


## Prerequisites
* [Colab][colab]: Throughout this lab we will use colab notebooks to run the labs. This is essential as the models will run much faster on the colab GPU compared to your personal laptops (which only have CPU). Please ensure you select the GPU runtime in Colab. 

## Instructions
Please upload your short report in the form of `firstname_lastname.pdf` (e.g. `georgia_gkioxari.pdf`) to this [dropbox link][dropbox] by Sunday, April 18. The length of the report should not exceed 2 pages and it should address the questions answered below.

## Part A: Silhouette Rendering

In Part 3A of [tutorial][py3dlab], you are asked to deform the vertices of an initial sphere mesh to fit a set of 2D silhouette views. 

1. Briefly explain what *silhouette rendering* is. 
2. What happens if you use 3 views instead of 20 views (`num_views = 20` in Dataset Creation)? Discuss the quality of the predicted shape.

## Part B: Textured Rendering

In Part 3B of [tutorial][py3dlab], you are asked to deform the vertices of an initial sphere mesh to fit a set of 2D textured views. Now the mesh consists of vertices, faces and vertex textures, meaning that for each vertex there is an RGB color associated with it. This type of texture is called `TexturesVertex`.

1. Briefly explain what the difference of *textured rendering* is compared to *silhouette rendering*. 
2. Instead of `TexturesVertex`, replace the texture type of the source mesh with [`TexturesUV`][textuv]. 
    1. Briefly describe what `TexturesUV` is and how it is different from `TexturesVertex`
    2. Provide the predicted `UV` texture map that you learnt when learning to optimize shape and texture via textured rendering with a `TexturesUV` texture type. (The texture map can be saved as an image.)


### Helpful material

- This short video [lecture][lecture] might be of help.
- The PyTorch3D [texturing API documentation][texdocs] might also be useful. 


[dropbox]: https://www.dropbox.com/request/Mk9FBIy7hJKe0f9hRdhv
[py3d]: https://github.com/facebookresearch/pytorch3d
[py3dtut]: https://github.com/facebookresearch/pytorch3d/tree/master/docs/tutorials
[py3dlab]: https://github.com/facebookresearch/pytorch3d/blob/master/docs/tutorials/fit_textured_mesh.ipynb
[colab]: https://colab.research.google.com/
[lecture]: https://www.youtube.com/watch?v=MOBAJb5nJRI&t=8189s
[textuv]: https://github.com/facebookresearch/pytorch3d/blob/master/pytorch3d/renderer/mesh/textures.py#L584
[texdocs]: https://github.com/facebookresearch/pytorch3d/blob/master/docs/notes/renderer_getting_started.md#texturing-options