
# Malaria Detector CNN

**Malaria Detector CNN** is a study about the diagnosis of malaria infection in a blood cell using CNNs (from scratch and pre-trained).

## Project information & contributors

All the code has been developed for the _Computational Intelligence and Deep Learning_ course at the university of Pisa by:
- [Francesca Pezzuti](https://github.com/fpezzuti)
- [Pietro Tempesti](https://github.com/PieTempesti98)

The **report** that describes the project in detail, and the **slides** are available here:
- [report](./report.pdf)
- [slides](./slides.pdf)

All the **code** is stored in the [Jupyter notebooks directory](./jupyter_notebooks/).

## Dataset

All the CNN models have been trained using the [malaria dataset](https://www.tensorflow.org/datasets/catalog/malaria?hl=en) from the Tensorflow catalogue.

Here is an example of cells infected and uninfected by malaria desease:

![Dataset](https://github.com/fpezzuti/MalariaDetector/assets/75533556/219716b2-484a-4832-abac-94baf84f510e)

The **malaria dataset** has the following **characteristics**:
- 2 **classes**: uninfected & parasitized
- 27558 **images**, perfectly **balanced**
- **Weight**: 317.62MB

## Results
CNN from scratch's results are **comparable to state-of-the-art** approaches:
- despite its simple architecture, our optimized CNN has **competitive performances** compared to literature approaches
- on the other ahnd, pur pre-trained models' results are not satisfactory
- a further improvement may be to leverage other pre-trained models

The results obtained by our best architecture are these:

| | Precision Recall | F1-Score | Support |
| --- | --- | --- | --- |
| Parasitized | 0.9749 | 0.9319 | 0.9529 | 2086 |
| Uninfected | 0.9336 | 0.9756 | 0.9542 | 2048 |
| Accuracy | | | 0.9536 | 4134 |
| Macro Avg | 0.9543 | 0.9538 | 0.9535 | 4134 | 
| Weighted Avg | 0.9545 | 0.9536 | 0.9535 | 4134 |

## XAI - CAM visualization
**CAM visualization** is a popular technique for interpreting the decisions of CNNs and can help identify which parts of an
image the network is attending to for classification.

We used _CAM visualization_ in order to identify possible classification patterns exploitable by medical experts to better assess their diagnoses.

![Explainable AI](https://github.com/fpezzuti/MalariaDetector/assets/75533556/b8dd45f0-13b8-4560-9b75-74b9106c8bdb)

For more details, refer to the Jupyter notebook about CAM visualization available [here](./jupyter_notebooks/CAM_visualization.ipynb).
