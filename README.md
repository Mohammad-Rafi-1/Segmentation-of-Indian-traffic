# Segmentation-of-Indian-traffic
In this we used two models for segmention task
1) Unet 
2) CAMnet


we initialized the Unet which is totally trained on Imagenet dataset and we used the concept of transfer learning on Unet to achieve segmentation. In second model we build entire CAMnet architecture from scratch which has less number of parameters when compares to Unet model to achieve the same segmentation task

## 1) Unet architecture

         you can refer this : https://arxiv.org/abs/1505.04597

   ![alt text](https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/u-net-architecture.png)

              *Total params: 62,980,990*

              *Trainable params: 62,879,224*

              *Non-trainable params: 101,766*


## 2) CAMnet architecture

      you can refer this : https://arxiv.org/pdf/2002.12041.pdf
  
  ![alt text](https://i.imgur.com/prH3Mno.png)

                *Total params: 160,245*

                *Trainable params: 159,269*

                *Non-trainable params: 976*

## Loss function

Dice loss = 1 - dice coefficient

where dice coefficient = 2TP/(2TP+FP+FN) 

Range of a loss function is {0,1}

If model predicts  all True Positives correctly then dice coefficient will be 1 and dice loss becomes 0  else dice loss will be in between {0,1} 

we can use cross-entropy loss as well but it is sensitive to imbalance dataset , In image segmentation we will deal with images which are having imbalanced labels because of this cross-entropy will not give proper measurement of True positives, people often use dice loss or iou loss for image segmentation task which penalizes the false positives and measure the True positive rate efficiently when compares to cross entropy , they are more robust to imbalance data and it can be  differentiable where we can easily back-propagate to updates weights

## Results

we trained camnet on less number of epoches when compares to Unet model on indian traffic dataset 

it giving  accurate results as Unet

if we train CAMnet for more no of epochs it will perform same task very effectively with less number of parameters when compares to Unet
