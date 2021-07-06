# Deep Learning Project MVP

An initial classification model was built to classify handwritten word images with the top 10 most frequent classes, which include:
* "
* ,
* .	
* a	
* and
* in
* of
* the
* to
* was

The model parameters are as follows:
```
#Build baseline model
base_model = mobilenet_v2.MobileNetV2(weights='imagenet', include_top=False, input_shape=(256,256,3)) 

#Freeze convolutional layers
for layer in base_model.layers:
    layer.trainable = False  

NN_transfer = Sequential(
                        [InputLayer(input_shape=(256,256,3)),
                         base_model,
                         Flatten(),
                         Dense(1000, activation='relu'),
                         Dense(1000, activation='relu'),
                         Dense(10, activation='softmax')]
                       )

NN_transfer.compile(
    loss='categorical_crossentropy',
    optimizer='adam',
    metrics=['accuracy'],
)

NN_transfer.fit_generator(generator=images_train, epochs=4, verbose=1)
```

The model is still training, however, the accuracy is above 90%. 