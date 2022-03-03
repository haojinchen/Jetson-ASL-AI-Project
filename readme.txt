Hello, this is a Jupyter Notebook File script built on top of Nvidia's Deep Learning institute's interactive classification tool code to classify basic American Sign Language images. This code is only trained for the letters A, B, C, and D but can be expanded to classify as many hand sign as wanted given enough training.

To run this Jupyter Notebook code, ssh into a device running NVIDIA's JetPack SDK image (Jetson Nano was the device used) with a usb camera and enter the docker with the following code 

		# create a reusable script
		echo "sudo docker run --runtime nvidia -it --rm --network host \
		    --volume ~/nvdli-data:/nvdli-nano/data \
		    --device /dev/video0 \
		    nvcr.io/nvidia/dli/dli-nano-ai:v2.0.1-r32.6.1" > docker_dli_run.sh

		# make the script executable
		chmod +x docker_dli_run.sh

		# run the script
		./docker_dli_run.sh

Once inside the docker, you may run this code and start building the convolutional neural network. Once that is completed, you may now start collected your own data for your ASL signing and train the CNN. If you are unsatisfied with the result, try collecting more images and train the model with more epocs.

More information about AI using a Jetson Nano computing unit can be found in the following link where you can find a free course going over the concept of AI image recognition 

	https://courses.nvidia.com/courses/course-v1:DLI+S-RX-02+V2/about