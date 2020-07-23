## Deliverables:
1. Overall val accuracy and class wise accuracies: Validation and Class wise accuracies are mentioned in notebook.
2. Summary of the methods you tried and what worked the best, if given more time how can we make it better:
  I first tried mobilenet because of the limitation in parameter(below 3M), but I wanted to try densenet because it works better for fine grained features and the images in dataset had finegrained features. So, I first tried to build Densnet but in between I realised that I will not be able to weights in that custom model. Then I tried to reverse engineer the densenet from torchvision but couldn't reduce the no. of parameters beyond a point which actually was graeter than 4M because of the shapes mismatch errors.
  Given more time, I can do a lot of things:
  1. Will try to remove more layers from densenet to reduce the size but it would have taken some time, It took me 3 hrs to do what I have done.
  2. I have definyely used [self-supervised methods](https://lilianweng.github.io/lil-log/2019/11/10/self-supervised-learning.html) to learn better representations from the data(Currently, I am working on this for 1 month in my current internship) and I am sure, It would have given much better result.
  3. I think I may also experimented with K-fold cross validation and pseudo labels because I have experimented with this on Kaggle for a image classification competition.
  
