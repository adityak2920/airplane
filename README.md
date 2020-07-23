## Deliverables:
1. Overall val accuracy and class wise accuracies: Validation and Class wise accuracies are mentioned in notebook.
2. Summary of the methods you tried and what worked the best, if given more time how can we make it better:
  I first tried mobilenet because of the limitation in parameter(below 3M), but I wanted to try densenet because it works better for fine grained features and the images in dataset had finegrained features. So, I first tried to build Densnet but in between I realised that I will not be able to use imagenet weights in that custom model. Then I tried to reverse engineer the densenet from torchvision but couldn't reduce the no. of parameters beyond a point which actually was greater than 4M because of the shapes mismatch errors.
    Given more time, I can do a lot of things:
    1. Will try to remove more layers from densenet to reduce the size but it would have taken some time, It was taking a lot of time in reverse engineering densenet.
    2. Given more time we can try [self-supervised methods](https://lilianweng.github.io/lil-log/2019/11/10/self-supervised-learning.html) to learn better representations from the data(Currently, I am working on this for 1 month in my current internship) and I am sure, It would have given much better result.
    3. I think I may also experimented with K-fold cross validation and pseudo labels because I have experimented with this on Kaggle for a image classification competition.
    4. Some experimentation with the augmentation and preprocesssing can also work.
    5. We can also use attention to make model learn better representation by focusing on more differentiating features or we can also use senets(squeeze and excitation networks).
    6. We can also try super resolution to increase size of image because the size of image was very smalll, so that network can work learn better features.
3. Trained model and code snippet for inference:

    ```data_preprocess(pulse).ipynb :```  It includes code for matching variant with family and then craeting dataset with folder name as labels.
    
    ```model_training.ipynb:``` It includes code for training and all the experiments that I have done.
    
    ```inference.ipynb:``` Code snnipet for doing inference using fastai learner or pytorch model on a single image or on folder containing images.
    
    **Note: Please use "pure_model.pth", "pure_pyfast.pth" or "air_learner.pkl" for inference**
4. Code along with steps to reproduce the results: I have included ```requirements.txt``` for the libraries necessary to run these notebooks. You can directly run each cell to reproduce each result.

The models are trained on Kaggle, so you can also check the notebook [here](https://www.kaggle.com/adityakumar01/kernel5fcffdd867?scriptVersionId=39385725)
  
