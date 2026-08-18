# 📱 Mobile Image Classification Using Pretrained Neural Networks

A MATLAB-based computer vision project that classifies images captured using a **mobile phone camera** with pretrained deep learning networks.

This project was developed as an **assignment applying the concepts learned during the Classify-X: Object Classification Workshop by MathWorks**.

## 🎯 Objective

To classify images captured using a mobile phone camera with pretrained deep learning networks in MATLAB.

The project uses **MATLAB Mobile** to capture images and applies pretrained neural networks to identify the objects present in those images.

## 🧠 Models Used

* **SqueezeNet** — used to classify three images captured through the mobile camera.
* **GoogLeNet** — used as a second pretrained neural network for comparison on an image.

Both networks are loaded using MATLAB's pretrained network functionality.

## ⚙️ Workflow

The overall workflow of the project is:

```text
Mobile Phone Camera
        ↓
   MATLAB Mobile
        ↓
   Capture Image
        ↓
   Resize Image
        ↓
 Pretrained Neural Network
        ↓
    Prediction
        ↓
 Predicted Class + Score
```

## 🔬 Implementation

The project connects MATLAB to a mobile device camera using:

```matlab
m = mobiledev;
cam = camera(m,"back");
```

A pretrained SqueezeNet model is then loaded:

```matlab
[net,classNames] = imagePretrainedNetwork("squeezenet");
```

The captured image is resized according to the network's required input size before prediction.

The prediction scores are converted into a class label and confidence score using:

```matlab
[label,score] = scores2label(scores,classNames);
```

The same approach is also demonstrated using **GoogLeNet** as a second pretrained network.

## 📊 Results

Three images were captured using the mobile phone camera and classified using SqueezeNet.

| Image   | Predicted Class |   Score |
| ------- | --------------- | ------: |
| Image 1 | Mouse           | 0.62658 |
| Image 2 | Laptop          | 0.49345 |
| Image 3 | Water Bottle    | 0.46294 |

GoogLeNet was also tested on Image 1 as an additional pretrained model.

## 🛠️ Technologies Used

* MATLAB
* MATLAB Mobile
* Deep Learning
* Image Processing
* Computer Vision
* Pretrained Neural Networks
* SqueezeNet
* GoogLeNet
* 
> Update the filenames above according to the actual files you upload to the repository.

## 📚 Learning Context

This project was created as an assignment to **implement and apply the knowledge gained from the Classify-X: Object Classification Workshop by MathWorks**.

The workshop helped provide practical exposure to object classification and the use of deep learning techniques for image-based applications.

## 🚀 Key Takeaways

Through this project, I gained practical experience with:

* Capturing images using a mobile device through MATLAB Mobile
* Preprocessing images for neural network input
* Using pretrained deep learning networks
* Performing image classification
* Interpreting prediction scores
* Comparing different pretrained architectures
* Applying workshop concepts to a practical assignment

## 👩‍💻 Author

**Sampriti Bhuniya**
CSE (AI)
University of Engineering & Management, Kolkata

---

⭐ If you find this project interesting, feel free to explore the code and results!
