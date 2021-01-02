#Chapter1
- Instead of telling computer the exact steps to solve a problem, show examples of the problems to solve and let it figure out itself.
- universal approximation theorem - can solve problem with right set of weights
- Limitation of weighted approach:
    - without data we cannot create models
    - labeled data is limited
    - predictive positive loop - more the model is used, more the data will become biased (based on environment) polocing as an example.

- Overfit & properfit
    - Even when your model has not fully memorized all your data, earlier on in training it may have memorized certain parts of it. 
    - As  a result, the longer you train for, the better your accuracy will get on the training set; 
    - The validation set accuracy will also improve for a while, but eventually it will start getting worse as the model starts to      memorize the training set, 
    - Rather than finding generalizable underlying patterns in the data. When this happens, we say that the model is overfitting.

- Transforms
    - `item_tfms` are applied to each item
    - `batch_tfms` are applied to a *batch* of items at a time using the GPU, so they're particularly fast

- CNN - Convolutional Nural Network 
    - High grade learner for vision requirements
    - Based on how human vision work

Resnet34
    - 34 layered architecture

epoh 
    - Number of passes completed by the algorithm on the training data

loss vs metric - Different coz of their purpose
    - Metric 
        - Error Rate
        - Accuracy = 1- error rate
        - A good choice is something which is easy for human  beings to consume
    - Loss
        - Defines measure of performance that training system can use to update the weights automatically
        - A good choice of loss is something that is easy for SGD to consume

- PreTrained Model: 
    - A model that has weights that have already been trained on some other dataset
    - fast ai cnn_learner has a parameter 'pretrained' defaulted to TRUE as it is been executed on millions of images

- Transfer Learning
    - Using a pretrained model for a task different to what it was originally trained for is known as transfer learning. 
    - Unfortunately, because transfer learning is so under-studied, few domains have pretrained models available.
    - For instance, there are currently few pretrained models available in medicine, making transfer learning challenging to use in that domain. 
    - In addition, it is not yet well understood how to use transfer learning for tasks such as time series analysis.

- Fine-tuning: 
    - A transfer learning technique where the parameters of a pretrained model are updated by training for additional epochs using a different task to that used for pretraining.
