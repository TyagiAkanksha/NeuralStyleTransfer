# NeuralStyleTransfer
  Neural style transfer is a technique used to apply the style of one image to the content of another image. It involves the use of deep neural networks to analyze the style and content of two images and then create a new image that combines them. The model is typically based on the VGG19 or other convolutional neural network architectures.

The process of neural style transfer involves three main steps:

1. Extracting features from the content image and style image using the convolutional neural network.

2. Comparing the content features of the content image to the style features of the style image to determine how to blend the two images.

3. Generating a new image that combines the content of the content image with the style of the style image by applying the blending information obtained in step 2 to the content image.

The result is an image that looks like the original content image but has been stylized with the texture, colors, and other visual features of the style image.

Neural style transfer has been used in various applications, such as art generation, image editing, and even in creating visual effects in movies. It allows for creative expression and can help artists and designers explo

## 1. Loading Pretrained Vgg19 Model
## 2. Preprocess the image
## 3. Deprocess the image
## 4. Get content,style features and create gram matrix 
## 5.  Creating Style and Content loss function
## 6. Training loop



