# Instructions
Please upload a txt file in the form of `firstname_lastname.txt`, e.g. `georgia_gkioxari.txt`. Each line will have your answer to the corresponding question, e.g. `Q1: 1`. Note that there can be multiple correct answers per question, in which case separate your answers with a comma, e.g. `Q1: 1, 2, 3`. Example file:
```
Q1: 1
Q2: 1, 2
Q3: 3, 4
...
```
Upload your answers to this [dropbox link][dropbox] by Sunday, April 18. 

# Test
### Question 1
A mesh is a collection of points without any connectivity between the points
  1. True
  2. False 

### Question 2
Which 3D representation is most efficient when aiming to capture high resolution object shapes
  1. Voxels
  2. Pointclous 

### Question 3
You have a shape which consists of parts of fine structure. What is the most appropriate 3D representation 
  1. Voxels
  2. Meshes

### Question 4
The chamfer distance measures the distance between
  1. Two voxels
  2. Two pointclouds

### Question 5
[Mesh R-CNN][meshrcnn] predicts 3D object shapes from single 2D images
  1. True
  2. False

### Question 6
In [Mesh R-CNN][meshrcnn], the topology of the predicted object is defined by the mesh-refinement branch
  1. True
  2. False

### Question 7
In [Mesh R-CNN][meshrcnn], `vert align` maintains the spatial alignment between the image features and the 3D mesh
  1. True
  2. False

### Question 8
When training models that predict meshes, adding shape regularizers to the objective leads to 
  1. More accurate predictions
  2. Prettier predictions

### Question 9
A distance between two pointclouds can be used as a distance between two meshes via
  1. differentiable mesh rendering
  2. differentiable point sampling on the mesh faces
  3. converting pointclouds and meshs to voxels

### Question 10
[Pointnet][pointnet] takes as input 2D images and predicts 3D pointclouds
  1. True
  2. False

### Question 11
[Pointnet][pointnet] is sensitive to the order of 3D points 
  1. True
  2. False

### Question 12
In [Occnets][occnet], the 3D representation used at train time is
  1. 3D meshes
  2. Signed distance functions (SDFs)
  3. Voxels

### Question 13
Differentiable mesh rendering allows for gradients to propagate back from a 2D loss to a 3D mesh
  1. True
  2. False

### Question 14
In [NMR][nmr], the 3D shapes are predicted by computing a loss between
  1. 2D shilhouettes
  2. 3D pointclouds
  3. 3D meshes

### Question 15
In [Mesh R-CNN][meshrcnn], a mesh subdivision followed by a graph convolution results in 
  1. increasing the receptive field
  2. decreasing the receiptive field
  3. none of the above


[dropbox]: https://www.dropbox.com/request/mdR1orxLo5hPs4wbkStV
[nmr]: https://arxiv.org/abs/1711.07566
[meshrcnn]: https://arxiv.org/abs/1906.02739
[r2n2]: https://arxiv.org/abs/1604.00449
[occnet]: https://arxiv.org/abs/1812.03828
[synsin]: https://arxiv.org/abs/1912.08804
[psg]: https://arxiv.org/abs/1612.00603
[pointnet]: https://arxiv.org/abs/1612.00593


