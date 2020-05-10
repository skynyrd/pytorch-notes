1. Tensors contain data of a uniform type (`dtype`)
2. Tensor computations between tensors depend on the `dtype` and `device`, which are both attributes of a torch Tensor.

```py
t1 = torch.tensor([1, 2, 3])
# t1. type --> torch.int64

t2 = torch.tensor([1., 2., 3.])
# t1. type --> torch.float32

# t1 + t2 --> runtime error
```

or

```py
t1 = torch.Tensor([1, 2, 3])  # device type: cpu
t2 = t1.cuda()                # device type: gpu

# t1 + t2 --> runtime error
```