🩺 Medical Caption Generation from Chest X-ray Images using Transformer-Based Attention Models

This project focuses on automated radiology report generation from chest X-ray images using deep learning and vision–language transformer models. Multiple architectures are implemented and compared, including traditional encoder–decoder models and advanced transformer-based models such as BLIP, GIT, and a custom ViT-T5 architecture.

The system is trained and evaluated on the IU Chest X-Ray dataset, generating clinically meaningful captions by learning the alignment between visual features and medical language.

📊 Dataset

IU Chest X-Ray Dataset (Indiana University)

      7,470 chest X-ray images
      
      3,955 radiology reports

Each report includes:

      Indication
      Comparison
      Findings
      Impression

⚙️ Data Preprocessing (data_cleaning.py)
    
      Merging projection and report CSV files
      Cleaning and normalizing medical text
      Combining Findings and Impression
      Adding special tokens: startseq, endseq
      Patient-level train / validation / test split
      Multi-view image pairing (frontal–lateral)
      Exporting structured CSV files for training

Output files:

      Train_Data.csv
      CV_Data.csv
      Test_Data.csv

🤖 ViT-T5 Model (vit_t5.py)

The proposed ViT-T5 architecture consists of:

      Vision Encoder: Vision Transformer (ViT)
      Bridge Module: Projection / Q-Former
      Text Decoder: T5 (Text-to-Text Transformer)
