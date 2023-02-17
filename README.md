# EVA-7

# Probelm Statement

* Check this Repo out: https://github.com/kuangliu/pytorch-cifar  
* You are going to follow the same structure for your Code from now on. So Create:
  * models folder - this is where you'll add all of your future models. Copy resnet.py into this folder, this file should only have ResNet 18/34 models. Delete Bottleneck Class
  * main.py - from Google Colab, now onwards, this is the file that you'll import (along with the model). Your main file shall be able to take these params or you should be able to pull functions from it and then perform operations, like (including but not limited to):
    * training and test loops
    * data split between test and train
    * epochs
    * batch size
    * which optimizer to run
    * do we run a scheduler?
  * utils.py file (or a folder later on when it expands) - this is where you will add all of your utilities like:
    * image transforms,
    * gradcam,
    * misclassification code,
    * tensorboard related stuff
    * advanced training policies, etc
    * etc
  * Name this main repos something, and don't call it Assignment 7. This is what you'll import for all the rest of the assignments. Add a proper readme describing all the files. 
* Your assignment is to build the above training structure. Train ResNet18 on Cifar10 for 20 Epochs. The assignment must:
  * pull your Github code to google colab (don't copy-paste code)
  * prove that you are following the above structure
  * that the code in your google collab notebook is NOTHING.. barely anything. There should not be any function or class that you can define in your Google Colab Notebook. Everything must be imported from all of your other files
  * your colab file must:
    * train resnet18 for 20 epochs on the CIFAR10 dataset
    * show loss curves for test and train datasets
    * show a gallery of 10 misclassified images
    * show gradcamLinks to an external site. output on 10 misclassified images. Remember to apply GradCAM on a channel that is greater than 5px.
  * Once done, upload the code to GitHub, and share the code. This readme must link to the main repo so we can read your file structure. 
  * Train for 20 epochs
  * Get 10 misclassified images
  * Get 10 GradCam outputs on any misclassified images (remember that you MUST use the library we discussed in the class)
  * Apply these transforms while training:
  * RandomCrop(32, padding=4)
  * CutOut(16x16)


# Solution

* ResNet model is written in master repo
  *  ResNet.py link - https://github.com/ShriramGithub7/CNN-Master/blob/main/model/resnet.py
  <br><br>
* Data Transformation is applied as per the given requirement
  * utils folder has this dataTransform.py file. Link: https://github.com/ShriramGithub7/CNN-Master/blob/main/utils/dataTransform.py
 <br><br>
* Training / Testing code is written in master repo
  * Link for training and testing code: https://github.com/ShriramGithub7/CNN-Master/blob/main/main.py
  <br>
* Below are logs after training model:
<br>
  
  
    EPOCH: 1
    Loss=-578679342213168535772856320.00 Batch_id=781 Accuracy=11.92: 100%|██████████| 782/782 [00:57<00:00, 13.71it/s]
    Test set: Average loss: -643273166133897029931237376.0000, Accuracy: 1000/10000 (10.00%)

    EPOCH: 2
    Loss=nan Batch_id=781 Accuracy=9.93: 100%|██████████| 782/782 [00:52<00:00, 14.77it/s]
    Test set: Average loss: nan, Accuracy: 1000/10000 (10.00%)_


  
