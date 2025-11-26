# Finger Alphabet Recognition – Transfer Learning with EfficientNetB3
![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-lightgrey)
![NumPy](https://img.shields.io/badge/NumPy-Array-blue)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plotting-brightgreen)

---

This educational ML project applies transfer learning to classify finger-alphabet hand signs.
It focuses on building a small but diverse dataset and applying modern deep-learning techniques.
---

### 🎓 Project Background
Key steps in the project:

- creating a custom dataset  
- preparing images for transfer learning  
- experimenting with several CNN architectures  
- training and fine-tuning the model  
- evaluating and analyzing performance  

Goal: Gain practical experience with computer vision, transfer learning, and dataset creation.

---

## 📚 Dataset

The dataset was **created entirely by our group** of eight participants.

<img width="567" height="340" alt="Bildschirmfoto 2025-11-25 um 22 24 06" src="https://github.com/user-attachments/assets/d2f09148-53c9-4316-8960-f8f56fc14d92" />



Our goals:
- build a **diverse** dataset (different hand shapes, skin tones, lighting, backgrounds)  
- ensure each member contributes their own images  
- keep the setup simple (smartphone photos)

At this stage, the dataset includes the first **three letters of the finger alphabet: A, B, C**.

### 🔒 Privacy Notice  
Because the dataset contains **participants’ hands**, I **do not share it publicly for privacy reasons**.  
If you want to **recreate the dataset**, discuss the setup, or **collaborate**, feel free to reach out.

---

## 🧠 Model & Training

### ✔️ Model Architecture

<img width="567" height="173" alt="Bildschirmfoto 2025-11-25 um 22 19 52" src="https://github.com/user-attachments/assets/26a98864-af80-4107-9c54-e5d629dd3f59" />

- **Backbone:** EfficientNetB3 (`include_top=False`)
- **Custom head:** Dense layers + Dropout
- **Loss:** categorical cross-entropy  
- **Optimizer:** Adam  
- **Metrics:** accuracy


### ✔️ Training Procedure
1. Load EfficientNetB3 pretrained on ImageNet  
2. Freeze base model  
3. Train custom classifier  
4. Unfreeze selected layers (fine-tuning)  
5. Train again with a lower learning rate

Typical parameters:
- batch size: 16  
- epochs: 60  
- augmentation: rotation, contrast, horizontal flip  

---

### 📈 Training Curves

<img width="276" height="210" alt="output" src="https://github.com/user-attachments/assets/6636914d-21e4-451b-a09f-989d6e462516" />
<img width="276" height="210" alt="output" src="https://github.com/user-attachments/assets/bce7594e-2add-4edb-b6fb-d7852cfbe74c" />


---

## 📈 Results

The model achieved strong performance on the three-class problem (A/B/C).  
You can find full metrics, plots, and confusion matrix in the notebook.


<p>
  <img width="227" height="192" alt="Bildschirmfoto 2025-11-25 um 22 39 02" src="https://github.com/user-attachments/assets/f0759e47-d6a7-4d2d-926d-1125f93e6762" />
  <img width="425" height="169" alt="Bildschirmfoto 2025-11-25 um 22 37 13" src="https://github.com/user-attachments/assets/5d65687e-13d7-4c71-8920-11bc8095e80e" />
</p>

You are welcome to extend the dataset and continue the model development.

---

## ▶️ Running the Notebook
This project runs entirely locally — no data is shared externally.

Install dependencies:

```
bash
pip install -r requirements.txt
```

Start the notebook:

```
bash
jupyter notebook Fingeralphabet_project.ipynb
```

⚠️ Note: The dataset used in this notebook is private. You can run the notebook with your own images or a recreated dataset.

---

## 🏁 Getting Started with a Dummy Dataset

If you want to run the notebook immediately **without the private dataset**:

1. **Create folders for the classes:**
   data/
A/
B/
C/


2. **Add any hand images** (or even placeholder images) into each folder.

3. **Update the notebook path** to point to your local `data/` folder.

4. **Run the notebook** — all steps (augmentation, training, evaluation) will work on this dummy dataset.

> This allows you to test the code and reproduce results **without using private data**.

---

## 🖼️ Example Output

Here’s what you can expect from running the notebook:

- **Training and validation accuracy curves**  
- **Loss curves** over epochs  
- **Confusion matrix** for the three classes  

---

## 📬 Contact / Collaboration

If you want to discuss the project, recreate the dataset, or collaborate:

- [GitHub](https://github.com/victoria-vasilieva)  
- [LinkedIn](https://www.linkedin.com/in/victoria-vasilieva/)
- v.vasiliewa@gmail.com 

Feel free to reach out — happy to share guidance or collaborate on extensions!
