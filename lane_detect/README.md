
```
wenhuizhangs-iMac:Models wenhuizhang$ python GCN.py 
Using Theano backend.
0  images are done
999  images are done
1998  images are done
2997  images are done
Shape of RGB:  (3001, 360, 800, 3)   Shape of Segmented:  (3001, 360, 800, 3)
__________________________________________________________________________________________________
Layer (type)                    Output Shape         Param #     Connected to                     
==================================================================================================
input_2 (InputLayer)            (None, 360, 800, 3)  0                                            
__________________________________________________________________________________________________
conv2d_1 (Conv2D)               (None, 360, 800, 4)  112         input_2[0][0]                    
__________________________________________________________________________________________________
batch_normalization_1 (BatchNor (None, 360, 800, 4)  16          conv2d_1[0][0]                   
__________________________________________________________________________________________________
leaky_re_lu_1 (LeakyReLU)       (None, 360, 800, 4)  0           batch_normalization_1[0][0]      
__________________________________________________________________________________________________
conv2d_2 (Conv2D)               (None, 360, 800, 10) 370         leaky_re_lu_1[0][0]              
__________________________________________________________________________________________________
max_pooling2d_1 (MaxPooling2D)  (None, 180, 400, 10) 0           conv2d_2[0][0]                   
__________________________________________________________________________________________________
conv2d_3 (Conv2D)               (None, 180, 400, 8)  728         max_pooling2d_1[0][0]            
__________________________________________________________________________________________________
batch_normalization_2 (BatchNor (None, 180, 400, 8)  32          conv2d_3[0][0]                   
__________________________________________________________________________________________________
leaky_re_lu_2 (LeakyReLU)       (None, 180, 400, 8)  0           batch_normalization_2[0][0]      
__________________________________________________________________________________________________
conv2d_4 (Conv2D)               (None, 180, 400, 15) 1095        leaky_re_lu_2[0][0]              
__________________________________________________________________________________________________
max_pooling2d_2 (MaxPooling2D)  (None, 90, 200, 15)  0           conv2d_4[0][0]                   
__________________________________________________________________________________________________
conv2d_5 (Conv2D)               (None, 90, 200, 16)  2176        max_pooling2d_2[0][0]            
__________________________________________________________________________________________________
batch_normalization_3 (BatchNor (None, 90, 200, 16)  64          conv2d_5[0][0]                   
__________________________________________________________________________________________________
leaky_re_lu_3 (LeakyReLU)       (None, 90, 200, 16)  0           batch_normalization_3[0][0]      
__________________________________________________________________________________________________
conv2d_6 (Conv2D)               (None, 90, 200, 20)  2900        leaky_re_lu_3[0][0]              
__________________________________________________________________________________________________
max_pooling2d_3 (MaxPooling2D)  (None, 45, 100, 20)  0           conv2d_6[0][0]                   
__________________________________________________________________________________________________
conv2d_7 (Conv2D)               (None, 45, 100, 32)  5792        max_pooling2d_3[0][0]            
__________________________________________________________________________________________________
batch_normalization_4 (BatchNor (None, 45, 100, 32)  128         conv2d_7[0][0]                   
__________________________________________________________________________________________________
leaky_re_lu_4 (LeakyReLU)       (None, 45, 100, 32)  0           batch_normalization_4[0][0]      
__________________________________________________________________________________________________
conv2d_8 (Conv2D)               (None, 45, 100, 30)  8670        leaky_re_lu_4[0][0]              
__________________________________________________________________________________________________
max_pooling2d_4 (MaxPooling2D)  (None, 22, 50, 30)   0           conv2d_8[0][0]                   
__________________________________________________________________________________________________
conv2d_9 (Conv2D)               (None, 22, 50, 40)   10840       max_pooling2d_4[0][0]            
__________________________________________________________________________________________________
batch_normalization_5 (BatchNor (None, 22, 50, 40)   160         conv2d_9[0][0]                   
__________________________________________________________________________________________________
leaky_re_lu_5 (LeakyReLU)       (None, 22, 50, 40)   0           batch_normalization_5[0][0]      
__________________________________________________________________________________________________
conv2d_10 (Conv2D)              (None, 22, 50, 50)   18050       leaky_re_lu_5[0][0]              
__________________________________________________________________________________________________
conv2d_11 (Conv2D)              (None, 22, 50, 30)   4530        conv2d_10[0][0]                  
__________________________________________________________________________________________________
conv2d_13 (Conv2D)              (None, 22, 50, 30)   4530        conv2d_10[0][0]                  
__________________________________________________________________________________________________
conv2d_12 (Conv2D)              (None, 22, 50, 30)   2730        conv2d_11[0][0]                  
__________________________________________________________________________________________________
conv2d_14 (Conv2D)              (None, 22, 50, 30)   2730        conv2d_13[0][0]                  
__________________________________________________________________________________________________
add_1 (Add)                     (None, 22, 50, 30)   0           conv2d_12[0][0]                  
                                                                 conv2d_14[0][0]                  
__________________________________________________________________________________________________
conv2d_15 (Conv2D)              (None, 22, 50, 30)   2730        add_1[0][0]                      
__________________________________________________________________________________________________
batch_normalization_6 (BatchNor (None, 22, 50, 30)   120         conv2d_15[0][0]                  
__________________________________________________________________________________________________
leaky_re_lu_6 (LeakyReLU)       (None, 22, 50, 30)   0           batch_normalization_6[0][0]      
__________________________________________________________________________________________________
conv2d_16 (Conv2D)              (None, 22, 50, 30)   2730        leaky_re_lu_6[0][0]              
__________________________________________________________________________________________________
add_2 (Add)                     (None, 22, 50, 30)   0           conv2d_16[0][0]                  
                                                                 add_1[0][0]                      
__________________________________________________________________________________________________
batch_normalization_7 (BatchNor (None, 22, 50, 30)   120         add_2[0][0]                      
__________________________________________________________________________________________________
leaky_re_lu_7 (LeakyReLU)       (None, 22, 50, 30)   0           batch_normalization_7[0][0]      
__________________________________________________________________________________________________
add_3 (Add)                     (None, 22, 50, 30)   0           leaky_re_lu_7[0][0]              
                                                                 max_pooling2d_4[0][0]            
__________________________________________________________________________________________________
conv2d_17 (Conv2D)              (None, 22, 50, 25)   2275        add_3[0][0]                      
__________________________________________________________________________________________________
conv2d_19 (Conv2D)              (None, 22, 50, 25)   2275        add_3[0][0]                      
__________________________________________________________________________________________________
conv2d_18 (Conv2D)              (None, 22, 50, 25)   1900        conv2d_17[0][0]                  
__________________________________________________________________________________________________
conv2d_20 (Conv2D)              (None, 22, 50, 25)   1900        conv2d_19[0][0]                  
__________________________________________________________________________________________________
add_4 (Add)                     (None, 22, 50, 25)   0           conv2d_18[0][0]                  
                                                                 conv2d_20[0][0]                  
__________________________________________________________________________________________________
conv2d_21 (Conv2D)              (None, 22, 50, 25)   1900        add_4[0][0]                      
__________________________________________________________________________________________________
batch_normalization_8 (BatchNor (None, 22, 50, 25)   100         conv2d_21[0][0]                  
__________________________________________________________________________________________________
leaky_re_lu_8 (LeakyReLU)       (None, 22, 50, 25)   0           batch_normalization_8[0][0]      
__________________________________________________________________________________________________
conv2d_22 (Conv2D)              (None, 22, 50, 25)   1900        leaky_re_lu_8[0][0]              
__________________________________________________________________________________________________
add_5 (Add)                     (None, 22, 50, 25)   0           conv2d_22[0][0]                  
                                                                 add_4[0][0]                      
__________________________________________________________________________________________________
conv2d_transpose_1 (Conv2DTrans (None, 45, 100, 20)  3020        add_5[0][0]                      
__________________________________________________________________________________________________
batch_normalization_9 (BatchNor (None, 45, 100, 20)  80          conv2d_transpose_1[0][0]         
__________________________________________________________________________________________________
leaky_re_lu_9 (LeakyReLU)       (None, 45, 100, 20)  0           batch_normalization_9[0][0]      
__________________________________________________________________________________________________
add_6 (Add)                     (None, 45, 100, 20)  0           leaky_re_lu_9[0][0]              
                                                                 max_pooling2d_3[0][0]            
__________________________________________________________________________________________________
conv2d_23 (Conv2D)              (None, 45, 100, 25)  1525        add_6[0][0]                      
__________________________________________________________________________________________________
conv2d_25 (Conv2D)              (None, 45, 100, 25)  1525        add_6[0][0]                      
__________________________________________________________________________________________________
conv2d_24 (Conv2D)              (None, 45, 100, 25)  1900        conv2d_23[0][0]                  
__________________________________________________________________________________________________
conv2d_26 (Conv2D)              (None, 45, 100, 25)  1900        conv2d_25[0][0]                  
__________________________________________________________________________________________________
add_7 (Add)                     (None, 45, 100, 25)  0           conv2d_24[0][0]                  
                                                                 conv2d_26[0][0]                  
__________________________________________________________________________________________________
conv2d_27 (Conv2D)              (None, 45, 100, 25)  1900        add_7[0][0]                      
__________________________________________________________________________________________________
batch_normalization_10 (BatchNo (None, 45, 100, 25)  100         conv2d_27[0][0]                  
__________________________________________________________________________________________________
leaky_re_lu_10 (LeakyReLU)      (None, 45, 100, 25)  0           batch_normalization_10[0][0]     
__________________________________________________________________________________________________
conv2d_28 (Conv2D)              (None, 45, 100, 25)  1900        leaky_re_lu_10[0][0]             
__________________________________________________________________________________________________
add_8 (Add)                     (None, 45, 100, 25)  0           conv2d_28[0][0]                  
                                                                 add_7[0][0]                      
__________________________________________________________________________________________________
conv2d_transpose_2 (Conv2DTrans (None, 90, 200, 15)  1515        add_8[0][0]                      
__________________________________________________________________________________________________
batch_normalization_11 (BatchNo (None, 90, 200, 15)  60          conv2d_transpose_2[0][0]         
__________________________________________________________________________________________________
leaky_re_lu_11 (LeakyReLU)      (None, 90, 200, 15)  0           batch_normalization_11[0][0]     
__________________________________________________________________________________________________
add_9 (Add)                     (None, 90, 200, 15)  0           leaky_re_lu_11[0][0]             
                                                                 max_pooling2d_2[0][0]            
__________________________________________________________________________________________________
conv2d_29 (Conv2D)              (None, 90, 200, 20)  920         add_9[0][0]                      
__________________________________________________________________________________________________
conv2d_31 (Conv2D)              (None, 90, 200, 20)  920         add_9[0][0]                      
__________________________________________________________________________________________________
conv2d_30 (Conv2D)              (None, 90, 200, 20)  1220        conv2d_29[0][0]                  
__________________________________________________________________________________________________
conv2d_32 (Conv2D)              (None, 90, 200, 20)  1220        conv2d_31[0][0]                  
__________________________________________________________________________________________________
add_10 (Add)                    (None, 90, 200, 20)  0           conv2d_30[0][0]                  
                                                                 conv2d_32[0][0]                  
__________________________________________________________________________________________________
conv2d_33 (Conv2D)              (None, 90, 200, 20)  1220        add_10[0][0]                     
__________________________________________________________________________________________________
batch_normalization_12 (BatchNo (None, 90, 200, 20)  80          conv2d_33[0][0]                  
__________________________________________________________________________________________________
leaky_re_lu_12 (LeakyReLU)      (None, 90, 200, 20)  0           batch_normalization_12[0][0]     
__________________________________________________________________________________________________
conv2d_34 (Conv2D)              (None, 90, 200, 20)  1220        leaky_re_lu_12[0][0]             
__________________________________________________________________________________________________
add_11 (Add)                    (None, 90, 200, 20)  0           conv2d_34[0][0]                  
                                                                 add_10[0][0]                     
__________________________________________________________________________________________________
conv2d_transpose_3 (Conv2DTrans (None, 180, 400, 10) 810         add_11[0][0]                     
__________________________________________________________________________________________________
batch_normalization_13 (BatchNo (None, 180, 400, 10) 40          conv2d_transpose_3[0][0]         
__________________________________________________________________________________________________
leaky_re_lu_13 (LeakyReLU)      (None, 180, 400, 10) 0           batch_normalization_13[0][0]     
__________________________________________________________________________________________________
add_12 (Add)                    (None, 180, 400, 10) 0           leaky_re_lu_13[0][0]             
                                                                 max_pooling2d_1[0][0]            
__________________________________________________________________________________________________
conv2d_35 (Conv2D)              (None, 180, 400, 15) 465         add_12[0][0]                     
__________________________________________________________________________________________________
conv2d_37 (Conv2D)              (None, 180, 400, 15) 465         add_12[0][0]                     
__________________________________________________________________________________________________
conv2d_36 (Conv2D)              (None, 180, 400, 15) 690         conv2d_35[0][0]                  
__________________________________________________________________________________________________
conv2d_38 (Conv2D)              (None, 180, 400, 15) 690         conv2d_37[0][0]                  
__________________________________________________________________________________________________
add_13 (Add)                    (None, 180, 400, 15) 0           conv2d_36[0][0]                  
                                                                 conv2d_38[0][0]                  
__________________________________________________________________________________________________
conv2d_39 (Conv2D)              (None, 180, 400, 15) 690         add_13[0][0]                     
__________________________________________________________________________________________________
batch_normalization_14 (BatchNo (None, 180, 400, 15) 60          conv2d_39[0][0]                  
__________________________________________________________________________________________________
leaky_re_lu_14 (LeakyReLU)      (None, 180, 400, 15) 0           batch_normalization_14[0][0]     
__________________________________________________________________________________________________
conv2d_40 (Conv2D)              (None, 180, 400, 15) 690         leaky_re_lu_14[0][0]             
__________________________________________________________________________________________________
add_14 (Add)                    (None, 180, 400, 15) 0           conv2d_40[0][0]                  
                                                                 add_13[0][0]                     
__________________________________________________________________________________________________
conv2d_transpose_4 (Conv2DTrans (None, 360, 800, 3)  183         add_14[0][0]                     
__________________________________________________________________________________________________
batch_normalization_15 (BatchNo (None, 360, 800, 3)  12          conv2d_transpose_4[0][0]         
__________________________________________________________________________________________________
leaky_re_lu_15 (LeakyReLU)      (None, 360, 800, 3)  0           batch_normalization_15[0][0]     
__________________________________________________________________________________________________
conv2d_41 (Conv2D)              (None, 360, 800, 3)  30          leaky_re_lu_15[0][0]             
__________________________________________________________________________________________________
conv2d_43 (Conv2D)              (None, 360, 800, 3)  30          leaky_re_lu_15[0][0]             
__________________________________________________________________________________________________
conv2d_42 (Conv2D)              (None, 360, 800, 3)  30          conv2d_41[0][0]                  
__________________________________________________________________________________________________
conv2d_44 (Conv2D)              (None, 360, 800, 3)  30          conv2d_43[0][0]                  
__________________________________________________________________________________________________
add_15 (Add)                    (None, 360, 800, 3)  0           conv2d_42[0][0]                  
                                                                 conv2d_44[0][0]                  
__________________________________________________________________________________________________
conv2d_45 (Conv2D)              (None, 360, 800, 3)  30          add_15[0][0]                     
__________________________________________________________________________________________________
batch_normalization_16 (BatchNo (None, 360, 800, 3)  12          conv2d_45[0][0]                  
__________________________________________________________________________________________________
leaky_re_lu_16 (LeakyReLU)      (None, 360, 800, 3)  0           batch_normalization_16[0][0]     
__________________________________________________________________________________________________
conv2d_46 (Conv2D)              (None, 360, 800, 3)  30          leaky_re_lu_16[0][0]             
__________________________________________________________________________________________________
add_16 (Add)                    (None, 360, 800, 3)  0           conv2d_46[0][0]                  
                                                                 add_15[0][0]                     
==================================================================================================
Total params: 110,815
Trainable params: 110,223
Non-trainable params: 592
__________________________________________________________________________________________________
Train on 1920 samples, validate on 480 samples
Epoch 1/40
1920/1920 [==============================] - 225999s 118s/step - loss: 1470.8708 - categorical_accuracy: 0.2455 - val_loss: 1156.3076 - val_categorical_accuracy: 0.2608
Epoch 2/40
1920/1920 [==============================] - 2604s 1s/step - loss: 1007.4608 - categorical_accuracy: 0.2752 - val_loss: 772.7570 - val_categorical_accuracy: 0.2715
Epoch 3/40
1920/1920 [==============================] - 2750s 1s/step - loss: 482.8078 - categorical_accuracy: 0.2763 - val_loss: 373.7214 - val_categorical_accuracy: 0.2741
Epoch 4/40
1920/1920 [==============================] - 2776s 1s/step - loss: 246.1707 - categorical_accuracy: 0.2770 - val_loss: 305.2242 - val_categorical_accuracy: 0.2667
Epoch 5/40
1920/1920 [==============================] - 2589s 1s/step - loss: 197.9336 - categorical_accuracy: 0.2765 - val_loss: 630.4654 - val_categorical_accuracy: 0.2336
Epoch 6/40
1920/1920 [==============================] - 2585s 1s/step - loss: 156.3120 - categorical_accuracy: 0.2784 - val_loss: 221.9444 - val_categorical_accuracy: 0.2718
Epoch 7/40
1920/1920 [==============================] - 2585s 1s/step - loss: 122.5918 - categorical_accuracy: 0.2818 - val_loss: 321.3992 - val_categorical_accuracy: 0.2797
Epoch 8/40
1920/1920 [==============================] - 2586s 1s/step - loss: 115.7610 - categorical_accuracy: 0.2890 - val_loss: 117.9772 - val_categorical_accuracy: 0.2907
Epoch 9/40
1920/1920 [==============================] - 2639s 1s/step - loss: 106.8600 - categorical_accuracy: 0.3049 - val_loss: 136.4407 - val_categorical_accuracy: 0.2820
Epoch 10/40
1920/1920 [==============================] - 2842s 1s/step - loss: 106.7737 - categorical_accuracy: 0.3270 - val_loss: 206.3923 - val_categorical_accuracy: 0.4138
Epoch 11/40
1920/1920 [==============================] - 3118s 2s/step - loss: 98.9824 - categorical_accuracy: 0.3313 - val_loss: 120.0159 - val_categorical_accuracy: 0.3130
Epoch 12/40
1920/1920 [==============================] - 2964s 2s/step - loss: 95.6572 - categorical_accuracy: 0.3496 - val_loss: 146.9091 - val_categorical_accuracy: 0.3454
Epoch 13/40
1920/1920 [==============================] - 2925s 2s/step - loss: 92.0068 - categorical_accuracy: 0.3547 - val_loss: 588.5099 - val_categorical_accuracy: 0.3153
Epoch 14/40
1920/1920 [==============================] - 2881s 2s/step - loss: 91.5268 - categorical_accuracy: 0.3673 - val_loss: 137.1442 - val_categorical_accuracy: 0.3822
Epoch 15/40
1920/1920 [==============================] - 2783s 1s/step - loss: 86.6840 - categorical_accuracy: 0.3696 - val_loss: 144.7778 - val_categorical_accuracy: 0.4313
Epoch 16/40
1920/1920 [==============================] - 2683s 1s/step - loss: 92.0519 - categorical_accuracy: 0.3837 - val_loss: 1052.2587 - val_categorical_accuracy: 0.3638
Epoch 17/40
1920/1920 [==============================] - 2890s 2s/step - loss: 88.7006 - categorical_accuracy: 0.3794 - val_loss: 254.2983 - val_categorical_accuracy: 0.7072
Epoch 18/40
1920/1920 [==============================] - 2818s 1s/step - loss: 91.4395 - categorical_accuracy: 0.3815 - val_loss: 95.2362 - val_categorical_accuracy: 0.3992
Epoch 19/40
1920/1920 [==============================] - 2590s 1s/step - loss: 83.0146 - categorical_accuracy: 0.3912 - val_loss: 94.4787 - val_categorical_accuracy: 0.3924
Epoch 20/40
1920/1920 [==============================] - 2589s 1s/step - loss: 84.3865 - categorical_accuracy: 0.3763 - val_loss: 94.1473 - val_categorical_accuracy: 0.3782
Epoch 21/40
1920/1920 [==============================] - 2589s 1s/step - loss: 79.2044 - categorical_accuracy: 0.3788 - val_loss: 84.9308 - val_categorical_accuracy: 0.3109
Epoch 22/40
1920/1920 [==============================] - 2588s 1s/step - loss: 78.0191 - categorical_accuracy: 0.3703 - val_loss: 159.5693 - val_categorical_accuracy: 0.3964
Epoch 23/40
1920/1920 [==============================] - 2587s 1s/step - loss: 76.8320 - categorical_accuracy: 0.3895 - val_loss: 150.5259 - val_categorical_accuracy: 0.5803
Epoch 24/40
1920/1920 [==============================] - 2588s 1s/step - loss: 76.6198 - categorical_accuracy: 0.3672 - val_loss: 84.0060 - val_categorical_accuracy: 0.4159
Epoch 25/40
1920/1920 [==============================] - 2587s 1s/step - loss: 76.9521 - categorical_accuracy: 0.3891 - val_loss: 92.0980 - val_categorical_accuracy: 0.3631
Epoch 26/40
1920/1920 [==============================] - 2586s 1s/step - loss: 81.3200 - categorical_accuracy: 0.3713 - val_loss: 114.0984 - val_categorical_accuracy: 0.6177
Epoch 27/40
1920/1920 [==============================] - 2584s 1s/step - loss: 83.2402 - categorical_accuracy: 0.3751 - val_loss: 117.6818 - val_categorical_accuracy: 0.3538
Epoch 28/40
1920/1920 [==============================] - 2585s 1s/step - loss: 78.7268 - categorical_accuracy: 0.3730 - val_loss: 87.1322 - val_categorical_accuracy: 0.3754
Epoch 29/40
1920/1920 [==============================] - 2586s 1s/step - loss: 75.5896 - categorical_accuracy: 0.3804 - val_loss: 79.5542 - val_categorical_accuracy: 0.4957
Epoch 30/40
1920/1920 [==============================] - 2586s 1s/step - loss: 74.0924 - categorical_accuracy: 0.3756 - val_loss: 81.5597 - val_categorical_accuracy: 0.5031
Epoch 31/40
1920/1920 [==============================] - 2591s 1s/step - loss: 72.1720 - categorical_accuracy: 0.3659 - val_loss: 86.6180 - val_categorical_accuracy: 0.3226
Epoch 32/40
1920/1920 [==============================] - 2592s 1s/step - loss: 71.7427 - categorical_accuracy: 0.3830 - val_loss: 78.8493 - val_categorical_accuracy: 0.3865
Epoch 33/40
1920/1920 [==============================] - 2591s 1s/step - loss: 72.1484 - categorical_accuracy: 0.3832 - val_loss: 106.6358 - val_categorical_accuracy: 0.4808
Epoch 34/40
1920/1920 [==============================] - 2586s 1s/step - loss: 71.8809 - categorical_accuracy: 0.3789 - val_loss: 80.8990 - val_categorical_accuracy: 0.3902
Epoch 35/40
1920/1920 [==============================] - 2587s 1s/step - loss: 69.3850 - categorical_accuracy: 0.3776 - val_loss: 90.4146 - val_categorical_accuracy: 0.3698
Epoch 36/40
1920/1920 [==============================] - 2588s 1s/step - loss: 67.3208 - categorical_accuracy: 0.3863 - val_loss: 71.6152 - val_categorical_accuracy: 0.4285
Epoch 37/40
1920/1920 [==============================] - 2589s 1s/step - loss: 64.4877 - categorical_accuracy: 0.3464 - val_loss: 72.3494 - val_categorical_accuracy: 0.3757
Epoch 38/40
1920/1920 [==============================] - 2589s 1s/step - loss: 62.7200 - categorical_accuracy: 0.3549 - val_loss: 72.8075 - val_categorical_accuracy: 0.4225
Epoch 39/40
1920/1920 [==============================] - 2589s 1s/step - loss: 61.4659 - categorical_accuracy: 0.3367 - val_loss: 104.2458 - val_categorical_accuracy: 0.3430
Epoch 40/40
1920/1920 [==============================] - 2586s 1s/step - loss: 69.2593 - categorical_accuracy: 0.3604 - val_loss: 375.0684 - val_categorical_accuracy: 0.4328

```
