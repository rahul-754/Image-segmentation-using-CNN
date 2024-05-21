# 🖼️ Image Segmentation Using Detectron2 with ResNet-101 and Panoptic Segmentation

This project implements image segmentation using Detectron2 with a ResNet-101 backbone, focusing on panoptic segmentation. Panoptic segmentation combines both instance and semantic segmentation to classify each pixel in an image either as part of a known object or background.

## ✨ Features

- 📝 **Data Preparation:** Load and preprocess images for training and testing.
- 🧠 **Model Architecture:** Utilize Detectron2 with ResNet-101 for panoptic segmentation.
- 🎓 **Training:** Train the model using labeled datasets.
- 🧪 **Evaluation:** Evaluate the model's performance on test data.
- 🔍 **Prediction:** Predict segmentation masks for new images.
- 📊 **Visualization:** Visualize the original images, ground truth masks, and predicted masks.

## 🛠️ Technologies Used

- **Python:** Programming language.
- **Detectron2:** Facebook AI Research's next-generation library for object detection and segmentation.
- **OpenCV:** Library for image processing.
- **NumPy:** Library for numerical computations.
- **Matplotlib:** Library for plotting and visualization.

## 🚀 Prerequisites

- **Python:** v3.7 or later
- **Detectron2:** Latest version compatible with your setup
- **PyTorch:** v1.6 or later
- **OpenCV:** v4.x
- **NumPy:** v1.18 or later
- **Matplotlib:** v3.x

## 📥 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/image-segmentation-detectron2.git
   cd image-segmentation-detectron2
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Install Detectron2:**
   Follow the instructions on the [official Detectron2 installation guide](https://detectron2.readthedocs.io/en/latest/tutorials/install.html).

## 📚 Usage

1. **Prepare the dataset:**
   - Place your training images and corresponding masks in the `data/train/images` and `data/train/masks` directories, respectively.
   - Place your test images and corresponding masks in the `data/test/images` and `data/test/masks` directories, respectively.

2. **Train the model:**
   ```bash
   python src/train.py
   ```

3. **Evaluate the model:**
   ```bash
   python src/evaluate.py
   ```

4. **Predict segmentation masks for new images:**
   ```bash
   python src/predict.py --image path/to/image.jpg
   ```

5. **Visualize the results:**
   ```bash
   python src/visualize.py
   ```

## 🧠 Model Architecture

The model uses a ResNet-101 backbone with a panoptic segmentation head from Detectron2. This architecture efficiently combines instance segmentation and semantic segmentation tasks.

## 🎓 Training

1. **Hyperparameters:**
   - Learning rate: `0.00025`
   - Batch size: `2`
   - Epochs: `50`
   - Loss function: Combination of classification, box regression, and mask prediction losses
   - Optimizer: `AdamW`

2. **Training Procedure:**
   - Load and preprocess the training data.
   - Initialize the Detectron2 model with ResNet-101 backbone.
   - Train the model using the training data and validate on the validation set.
   - Save the best performing model.

## 🧪 Evaluation

- **Metrics:**
  - AP (Average Precision)
  - IoU (Intersection over Union)
  - PQ (Panoptic Quality)
- **Evaluation Procedure:**
  - Load the saved model.
  - Evaluate the model on the test dataset.
  - Calculate and display the evaluation metrics.

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the repository.**
2. **Create a new branch:**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes and commit them:**
   ```bash
   git commit -m 'Add new feature'
   ```
4. **Push to the branch:**
   ```bash
   git push origin feature/your-feature-name
   ```
5. **Create a new pull request.**

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## 📧 Contact

For any inquiries or issues, please contact [rahulkumar69953175@gmail.com].

---

Happy coding! 🚀
