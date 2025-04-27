# Defect_Detection

Dependencies

pip install torch torchvision opencv-python pillow numpy scikit-learn matplotlib

Inference
Run the shell script:

bash defect_detection_inf.sh

Or run the Python script directly:

python3 inference.py \
  --eval_json path/to/test.json \
  --checkpoint path/to/checkpoint.pth \
  --batch_size 8
  
--eval_json：Path to the validation JSON file.
--checkpoint：Path to the model checkpoint file.

Output Description
After inference, the console will display:
Overall Accuracy: 0.xxxx
Pass Accuracy:    0.xxxx
Fail Accuracy:    0.xxxx

In the project’s root directory two files will be created:

inference_results.json
A JSON file containing, for each image, the predicted label(s) and the ground-truth label(s).

confusion_matrix.png
A plot of the confusion matrix.
