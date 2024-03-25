Alzheimer’s disease (AD) is a progressive brain condition where memory and thinking abilities decline gradually and can't be reversed. Researchers have used various methods and computer programs to look for specific patterns in brain images to tell apart the different stages of AD. However, it's tough because the brain patterns in older adults and in different stages of AD can look very similar. This similarity makes it challenging for scientists to accurately classify the different stages of the disease using these methods.
Our aim was to categorize various stages of Alzheimer's disease.In this study, we utilized the convolutional neural network structures of pre-trained Inception V3 and 3D CNN and machine learning technique of XGboost to analyze MRI data from the OASIS database.Through the implementation of a deep learning algorithm, we successfully differentiated between four distinct stages of the disease, namely Mild Demented, Moderate Demented, Non-Demented, and Very Mild Demented.
CNN is really good at finding feature from different parts in MRI. But sometimes, the simple classifier used in CNN can get confused by extra proper feature in the picture, making it harder to classify things correctly. To fix this, we use a fancy model called XGBoost that combines lots of different classifiers together. This helps make sure we get the right classification even when there's extra feature in the picture. To better tell apart the features we get from images, we came up with a model called CNN-XGBoost for image classification. This special model combines two parts: First, there's the CNN, which finds the different parts in the pictures automatically. Then, there's XGBoost, which decides what those parts mean and puts them into categories. We fine-tuned this model to work well together and make sure it classifies images accurately. During our study, we developed 3 CNN models for feature extraction from image and passed through this extracted feature to XGbosst classifier for multi-classification. The prior two are 2D CNN using pre-trained Inception V3. Between them one model we used softmax activation in the final output layer and another one we didn’t used softmax activation in the output layer. By omitting softmax activation on the output layer of Inception V3 for MRI image feature extraction, we obtain continuous-valued features. This approach offers greater flexibility, interpretability, and potentially higher-quality features, while also reducing computational complexity. Results from our experiments show that this model works better compared to other methods found in existing research. And the final one we made 3D CNN without softmax Activation. 
Evaluation revealed a moderate accuracy of 55% and 51% for the 2D Inception V3 pre-trained and 3D CNN model without softmax activation function, indicating potential for improvement. Higher precision and recall were observed for non-demented cases, suggesting discriminatory capabilities. The Inception V3 pre-trained model with sotmax, integrated with XGBoost, achieved an impressive accuracy of 93% across all dementia stages, demonstrating the efficacy of the hybrid approach. Even though our present work has observed valuable outcomes, there is still room for improvement.
