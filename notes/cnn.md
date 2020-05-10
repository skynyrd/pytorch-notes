# CNN (Convolutional Neural Networks) Tensor Shape

* [?, ?, ?, ?]
* If it's an image, it's [BATCH_SIZE (OR NUMBER_OF_SAMPLES), COLOR_CHANNEL, HEIGHT, WIDTH]
* Color Channel is 1 for grey scale, 3 for RGB. 
* Height and Width are simply representing the resolution (but starting from height) e.g. 768, 1024
* BATCH_SIZE represents how many images a tensor have.

e.g. [3, 1, 28, 28] means there are 3 images, all are in grey scale and 28 * 28 (H * W)

* Suppose we have a tensor that contains data from a single 28 x 28 grayscale image. This gives us the following tensor shape: [1, 1, 28, 28].
* Now suppose this image is passed to our CNN and passes through the first convolutional layer. When this happens, the shape of our tensor and the underlying data will be changed by the convolution operation.
* The convolution changes the height and width dimensions as well as the number of channels. The number of output channels changes based on the number of filters being used in the convolutional layer.