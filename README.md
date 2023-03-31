# Neural Style Transfer
  Neural style transfer is a technique used to apply the style of one image to the content of another image. It involves the use of deep neural networks to analyze the style and content of two images and then create a new image that combines them. The model is typically based on the VGG19 or other convolutional neural network architectures.

The process of neural style transfer involves three main steps:

1. Extracting features from the content image and style image using the convolutional neural network.

2. Comparing the content features of the content image to the style features of the style image to determine how to blend the two images.

3. Generating a new image that combines the content of the content image with the style of the style image by applying the blending information obtained in step 2 to the content image.

The result is an image that looks like the original content image but has been stylized with the texture, colors, and other visual features of the style image.

Neural style transfer has been used in various applications, such as art generation, image editing, and even in creating visual effects in movies. It allows for creative expression and can help artists and designers explo

## 1. Loading Pretrained Vgg19 Model
     This steps involves downloading the pre-trained weights for the VGG19 architecture, and then loading them into a deep learning framework PyTorch. This allows the model to be used for various computer vision tasks without the need for training from scratch, and can save a lot of time and resources.
## 2. Preprocess the image
      Preprocessing an image involves transforming it into a format that can be input into a machine learning model, such as resizing, normalizing pixel values, and converting to a tensor. 
      This ensures that the model can properly interpret and analyze the image data.
## 3. Deprocess the image
      Deprocessing an image is the inverse operation of preprocessing, which involves converting the output of a deep learning model back into an image that can be visualized. 
      This often involves reversing the normalization and resizing operations applied during preprocessing, and converting the tensor back to an image format. 
      This allows the output of the model to be easily interpreted and analyzed.
## 4. Get content,style features and create gram matrix 
      To get content and style features, we pass the content and style images through a pre-trained CNN, such as VGG19, and extract the feature maps from one or more layers of the network.

       To create the gram matrix, we first vectorize the feature maps from a given layer and then calculate the outer product of each feature vector with itself, which gives us a matrix that represents the correlations between the different features.

        
        The resulting gram matrix is used to measure the style similarity between the style image and the generated image in neural style transfer algorithms.
      
## 5.  Creating Style and Content loss function
      In neural style transfer, the style loss function measures the difference between the gram matrices of the style image and the generated image at each layer of a pre-trained CNN, while the content loss function measures the difference between the feature maps of the content image and the generated image at a specific layer.

     These loss functions are combined with weights to create a total loss function, which is minimized during training to produce a generated image that matches the content of the content image while incorporating the style of the style image.

     By balancing the weights of the style and content loss functions, the generated image can be adjusted to emphasize either the content or style of the input images.
## 6. Training loop
      The training loop in neural style transfer involves initializing a generated image, calculating the style and content loss, and using an optimizer to minimize the total loss function with respect to the generated image. The process is repeated for a certain number of iterations or until a certain threshold is reached. The final generated image is then deprocessed to obtain the stylized output image, with the weights and number of iterations adjusted to achieve the desired level of stylization and fidelity to the input images.



