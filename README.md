# Clay Classification using Machine Learning

## Objective
The objective of this project is to classify different clay types based on experimentally measured physicochemical properties such as particle size distribution, chemical composition, and physical characteristics.

---

## Workflow / Pipeline

1. **Data Generation**  
   Experimental dataset collected from different clay samples.

2. **Preprocessing**  
   - Feature scaling (Standardization)  
   - Label encoding for clay categories  

3. **Modeling**  
   - Random Forest  
   - Support Vector Machine (SVM)  

4. **Evaluation**  
   - Accuracy score  
   - Confusion matrix  
   - Classification report  

5. **Visualization**  
   - Confusion matrix heatmap  
   - Feature importance (Random Forest)  

6. **Robustness Check**  
   - Noise perturbation added to input features to simulate measurement uncertainty  

---

## Dataset Description

The dataset consists of experimental measurements of clay samples, including:

- Particle size distribution: d10, d50, d90, span  
- Chemical composition: SiO₂, Al₂O₃, Fe₂O₃, CaO, MgO, LOI  
- Derived features: Al/Si ratio  
- Physical properties: water absorption  

Each sample is labeled with its corresponding clay type.

---

## Repository Structure

