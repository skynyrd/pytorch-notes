* GPU => CUDA => PyTorch => Apps
* moving tensor operations to GPU using CUDA

```py
import torch

t = torch.tensor([1, 2, 3])
print(t)

# uncomment the lines below if PyTorch CUDA version is installed.
# t = t.cuda()  # data transfer from CPU to GPU is expensive
# print(t)

```

* tensor => n dimentional array
* Rank of a tensor => number of dimensions present within the tensor. e.g. matrix, 2d-array or 2d-tensor (all are same)
* tensor size = tensor shape

```py
t = torch.tensor([1,2,3,4,5,6])

print(t)
print("\n")
print(t.reshape(2,3))
print("\n")
print(t.view(3,2))
```

* As the name suggests, torch.view merely creates a view of the original tensor. The new tensor will always share its data with the original tensor. This means that if you change the original tensor, the reshaped tensor will change and vice versa.
* torch.reshape doesn't impose any contiguity constraints, but also doesn't guarantee data sharing. The new tensor may be a view of the original tensor, or it may be a new tensor altogether.
* If you just want to reshape tensors, use torch.reshape. If you're also concerned about memory usage and want to ensure that the two tensors share the same data, use torch.view.