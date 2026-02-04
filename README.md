# 📌 Configurable Training Pipeline with Checkpointing

## 📖 Project Description
This project implements a configurable training pipeline using PyTorch.
Training parameters and file paths are managed through a YAML configuration file.
The pipeline supports checkpoint saving and resuming and logs training metrics to a CSV file for analysis.

## 🛠 Technologies Used
- Python
- PyTorch
- PyYAML
- CSV
- Google Colab

## 📂 Project Structure
├── Configurable_Training_Pipeline.ipynb
├── config.yaml
├── checkpoints/
│   └── model_epoch_X.pth
├── logs/
│   └── metrics.csv
└── README.md

## ⚙️ Configuration File (config.yaml)
The YAML file is used to configure:
Number of epochs
Batch size
Learning rate
Checkpoint directory
Log directory
Resume checkpoint path

To resume training, update: 
```yaml
resume_checkpoint: checkpoints/model_epoch_3.pth

▶️ How to Run
- Open the notebook in Google Colab
- Enable GPU:
         Runtime → Change runtime type → GPU (T4)
- Run all cells sequentially from top to bottom
- Training progress is printed per epoch
- Checkpoints are saved after every epoch
- Metrics are logged in logs/metrics.csv

💾 Checkpointing
- Model checkpoints are saved after each epoch
- Training can be resumed from the last saved checkpoint using config.yaml

📊 Metrics Logging
- Training loss and accuracy are stored in metrics.csv
- This file can be used for later analysis or plotting

✅ Output
- Console output showing epoch-wise loss and accuracy
- Saved model checkpoints
- CSV file containing training metrics
