The AI model developed for this project is designed to identify vehicles, drones, and humans from long distances, even under adverse conditions. It achieves an accuracy of 80% and is built using a combination of two convolutional neural network (CNN) layers (with 64 and 32 filters) and one artificial neural network (ANN) layer (128 and 3 neurons).
To optimize training, a callback list is employed, including features such as:
•	Model checkpoint: Monitors the validation accuracy, saving the best epoch.
•	Early stopping: Halts training if validation loss doesn’t improve for 15 epochs.
•	Reduce learning rate: Automatically reduces the Adam optimizer's learning rate if validation loss stagnates for 3 consecutive epochs.
For real-time image processing and predictions, OpenCV is used. 
To make the model robust against adversarial conditions, adversarial attacks were introduced during training using the Fast Gradient Method from the ART library. The training set consists of 50% adversarially attacked images, which have been distorted from their original state, and 50% regular images. This mixture allows the model to effectively predict blurred or long-distance images.
Due to the extensive time required for training with adversarially attacked images, the training process was not fully completed within the available time.



