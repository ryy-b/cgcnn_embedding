# GNN Embedding Visualization

visualize the crystal graph embedding of [CGCNN](#CGCNN) using t-SNE with value of formation energy

<br>

![embedding](latent.png)

<br>

# Dataset

CIF downloaded from the Materials Project [https://materialsproject.org/] with the following search criteria

```
data = mpr.query(
                 criteria={
                           "elements": {"$nin": ["He"]},
                           "nelements": {"$gt": 3},
                           "formation_energy_per_atom" : {"$gt" : -3},
                           },
                 properties=["cif", "formation_energy_per_atom"]
                )
```

<br>

# CGCNN
```
@article{PhysRevLett.120.145301,
  title = {Crystal Graph Convolutional Neural Networks for an Accurate and Interpretable Prediction of Material Properties},
  author = {Xie, Tian and Grossman, Jeffrey C.},
  journal = {Phys. Rev. Lett.},
  volume = {120},
  issue = {14},
  pages = {145301},
  numpages = {6},
  year = {2018},
  month = {Apr},
  publisher = {American Physical Society},
  doi = {10.1103/PhysRevLett.120.145301},
  url = {https://link.aps.org/doi/10.1103/PhysRevLett.120.145301}
}
```