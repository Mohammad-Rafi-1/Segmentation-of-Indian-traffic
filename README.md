# Segmentation-of-Indian-traffic
In this we used two models for segmention task
1) Unet 
2) CAMnet


we initialized the Unet which is totally trained on Imagenet dataset and we used the concept of transfer learning on Unet to achieve segmentation. In second model we build entire CAMnet architecture from scratch which has less number of parameters when compares to Unet model to achieve the same segmentation task

1) Unet architecture

   you can refer this : https://arxiv.org/abs/1505.04597

    ![alt text](https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/u-net-architecture.png)

              *Total params: 62,980,990*

              *Trainable params: 62,879,224*

              *Non-trainable params: 101,766*


2) CAMnet architecture

      you can refer this : https://arxiv.org/pdf/2002.12041.pdf
  
  ![alt text](https://i.imgur.com/prH3Mno.png)

                *Total params: 160,245*

                *Trainable params: 159,269*

                *Non-trainable params: 976*
