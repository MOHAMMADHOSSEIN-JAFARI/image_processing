# image_processing

The explanation is based on the code final_project.py and final_project_test.py. 
•	The code can generate a batch of Voronoi images. Each image is a PyTorch tensor with 3 dimensions which are [channel, height, width]. The dimension is [3, height, width] for RGB images, and for grayscale images, it is [1, height, width]
•	All images are stored in a PyTorch tensor named image_tensor which has 4 dimensions, which are [batch, channel, height, width].
•	It is possible to configure the followings: The Number of images, Image size, Number of randomly sampled points, Line Thickness, and the seed for all randomness, grayscale, or RGB images. 
•	It is known that the goal is to store the images as PyTorch tensors, and it is not needed to save images in .png format. Just to show that the code works correctly, the first image is converted from PyTorch tensor to an image in the format of img1.png
•	cell_Colors function colors each cell randomly. 
•	The boundary lines are the same for each image, and it is colored randomly by the boundary_Colors function.
•	The method of the script: Firstly, the needed information is gotten from the user. Based on the number of batches, a for loop is run for each image. With the help of the scipy.spatial which has Voronoi, voronoi_plot_2d, the image is generated in the format of matplotlib. Then the image is stored with the name of image.png in the directory where the script is run.  Then the image.png is opened as Grayscales or RGB and it is resized to the desired size. After that, it is transformed into a PyTorch tensor, and it is added to the image_tensor. Again, the for loop is run for the second image and it is overwritten on the previous image. Therefore, at each moment, just one image is in the directory. 
•	I have attached three images of generated pictures. 