# Homework 3

## Data Preparation

1. **Selecting Photos**:
   - Choose 9 photos of penguins to create my dataset. 
   <div align="center">
       <img width="888" alt="截圖 2024-06-26 凌晨12 15 34" src="https://github.com/mvclab-ntust-course/course3-lannyyuan-go/assets/122262894/44985b77-8efa-4c52-8597-b6582bf9c999">
   </div>

2. **Resizing Images**:
   - Use an image editing tool or script to resize all selected images to a uniform size of 512 x 512 pixels. This step ensures that the input data is consistent, which is crucial for training the model effectively.

3. **Generating Labels**:
   - Utilize the Dataset Maker tool from Kohya Colabs to generate corresponding labels for my images. 
     - Go to the [Dataset Maker repository](https://github.com/hollowstrawberry/kohya-colab).
     - Follow the instructions to install and set up the Dataset Maker tool.
     - Input my resized images to generate the necessary labels.

## Model Training and Image Generation

1. **Training the Model**:
   - I will use the Trainer tool from Kohya Colabs to train my model. Here’s how:
     - Access the Trainer tool from [Kohya Colabs](https://github.com/hollowstrawberry/kohya-colab).
     - Configure the training settings: set the number of epochs to 20.
     - Start the training process and monitor progress to ensure the model trains correctly.

2. **Using the Final Model with webUI**:
   - Once training is complete, take the final model from the last epoch and integrate it with the webUI.
     - Follow the installation guide specific to my operating system. For Mac users, refer to the guide on [iMaster](https://www.imaster.org/%e5%a6%82%e4%bd%95%e5%9c%a8-mac-%e4%b8%8a%e5%ae%89%e8%a3%9d-stable-diffusion-%e8%bb%9f%e9%ab%94%ef%bc%9f/) to install Stable Diffusion software.
     - Configure webUI to use the Lora model I trained.
     - Test the setup by using various prompts to generate images and ensure the model works as expected.
     
   <div align="center">
       <img width="888" alt="截圖 2024-06-25 下午6 32 36" src="https://github.com/mvclab-ntust-course/course3-lannyyuan-go/assets/122262894/d02bb18a-965e-4767-a7e7-90fcf0f05ebe">
   </div>
   <div align="center">
       <img width="888" alt="截圖 2024-06-25 下午6 39 41" src="https://github.com/mvclab-ntust-course/course3-lannyyuan-go/assets/122262894/d6bbc901-7108-49c4-baa7-6d0e36a538b6">
   </div>

## wandb Integration

1. **Setting Up wandb**:
   - Sign up for a [wandb account](https://wandb.ai/site) if I don’t have one.
   - Install the wandb Python package: `pip install wandb`.
   - Initialize wandb in my script:
     ```python
     import wandb
     wandb.init(project="my_project_name")
     ```

2. **Modifying Training Scripts**:
   - Manually modify the `train_network.py` and `train_network_wrapper.py` scripts from the Trainer tool to log metrics and results to wandb. 

3. **My Training Result**:
   
   <div align="center">
       <img width="426" alt="截圖 2024-06-26 凌晨12 19 26" src="https://github.com/mvclab-ntust-course/course3-lannyyuan-go/assets/122262894/0df150a8-aca0-4ef0-b93f-652749233cd1">
   </div>


