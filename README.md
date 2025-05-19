# NEURAL-STYLE-TRANSFER
COMPANY: CODETECH IT SOLUTIONS

NAME:SRAVAN JANGAM

INTERN ID: CODF209

DOMAIN: Artificial Intelligence Markup Language

DURATION: 4 WEEKS

MENTOR: NEELA SANTOSH

In this project, I implemented Neural Style Transfer using PyTorch to blend the visual content of one image with the artistic style of another. The core objective was to generate a new image that retains the structure and objects from the content image while replicating the textures, colors, and brushstrokes of the style image. The project was developed in a Jupyter Notebook using Python, with primary support from libraries such as PyTorch, TorchVision, Pillow, and Matplotlib. I used the pre-trained VGG19 convolutional neural network model from PyTorch’s torchvision.models. VGG19 is widely used for image processing tasks due to its deep architecture and effective feature extraction capabilities. The first step was loading and preprocessing the content and style images. I used the Pillow library to read the images and applied transformations such as resizing, cropping, normalization, and converting them to tensors using torchvision.transforms. This ensured compatibility with the VGG19 model, which expects input images in a specific shape and scale. After loading the images, I extracted features from specific layers of the VGG19 model. For content representation, I selected a deeper layer (like conv4_2) to capture high-level structures and objects. For style representation, I selected multiple layers (e.g., conv1_1, conv2_1, conv3_1, etc.) to capture patterns, textures, and stylistic features. To compute the loss and guide the optimization, I defined two primary loss functions: Content Loss: This was calculated as the Mean Squared Error (MSE) between the content features of the generated image and the original content image. Style Loss: This used the Gram matrix representation of the style features and measured the MSE between the style image and the generated image’s Gram matrices at various layers. These two losses were then combined using user-defined weights (commonly with a higher weight on style loss) to form a total loss function. The goal was to minimize this total loss during the optimization process. The generated image was initialized as a clone of the content image and updated using backpropagation. I used the L-BFGS optimizer from PyTorch's optim module, which is well-suited for style transfer due to its performance on loss surfaces with many local minima. The optimization loop repeatedly updated the generated image to minimize the total loss. After a set number of iterations, the resulting image was converted back from a tensor to a displayable format using inverse transformations. Finally, I visualized the content, style, and generated images using matplotlib.pyplot. This project helped me understand important deep learning concepts such as convolutional neural networks, feature maps, transfer learning, and gradient-based optimization.





OUTPUT:![Image](https://github.com/user-attachments/assets/616a85cf-3dce-42fa-8720-8137daca2e8b)
