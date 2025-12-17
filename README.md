# Cell-Classifier

# Overview

 -This project focuses on cellular image classification across multiple cell types using deep learning, with an emphasis on robust generalisation under limited labelled data—a common constraint in biomedical imaging.
 
 -The goal is to build and evaluate models capable of distinguishing between visually similar cellular structures while remaining resilient to data scarcity and annotation noise.
 
 -The current dataset is organised at the cell group level, with images grouped by biological category:

  Data/raw/
  
   ├── neuron/
   
   ├── phloem/
   
   ├── rbc/
   
   └── xylem/


 Each folder contains microscopy images corresponding to a specific cell group. These datasets serve as the primary supervised training and evaluation sources for this project.

# Key Challenge: Label Granularity

 A central challenge in this project is the limited availability of high-quality labels at the individual cell level. While cell group–level labels are available, fine-grained annotations for single cells within an image are scarce, inconsistent, or costly to obtain.
 
 This constraint influences:
 
  *Model architecture choices
  
  *Training strategy
  
  *Evaluation methodology
  
  *Rather than treating this as a limitation to be ignored, the project explicitly designs around this reality, aligning with real-world biomedical machine learning workflows.

Methodological Approach:

 *To mitigate label scarcity and improve feature robustness, the project adopts a representation-first learning strategy:
 
 *Supervised classification using available cell group labels
 
 *Transfer learning from encoders pretrained on related microscopy data
 
 *Exploration of self-supervised pretraining pipelines validated in a separate pilot project
 
 A preliminary methodological exploration using unlabelled microscopy data (Cellpose) is conducted in a separate trial repository to validate pretraining strategies before integration into this main project.

# 📊 Project Status

 ✅ Initial dataset organisation and exploration
 
 🔄 Model training and baseline evaluation
 
 ⏳ Integration of pretrained representations
 
 ⏳ Extended evaluation and ablation studies

Related Work:

 Cellpose Trial Project – Methodological exploration of self-supervised pretraining on unlabelled microscopy images (separate repository)
