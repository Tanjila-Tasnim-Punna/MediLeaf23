# 🌿 MediLeaf-23

**Leaf images of 23 medicinal plant categories collected in Bangladesh**

[![DOI](https://img.shields.io/badge/DOI-10.17632%2Fw9nnvf3t6p.1-00b894)](https://doi.org/10.17632/w9nnvf3t6p.1)
![Images](https://img.shields.io/badge/images-9%2C817-2c5364)
![Classes](https://img.shields.io/badge/classes-23-2c5364)
![License](https://img.shields.io/badge/license-CC_BY_4.0-lightgrey)

This repository holds the code and experiments for **MediLeaf-23**, an open image dataset for medicinal plant identification. The images themselves are hosted on **[Mendeley Data](https://doi.org/10.17632/w9nnvf3t6p.1)**.

## Dataset at a glance

| | |
|---|---|
| Images | 9,817 photos of single leaves |
| Classes | 23 medicinal plants |
| Location | Garden of Daffodil International University, Savar, Dhaka |
| Collected | September–October 2026 |
| Camera | iPhone 13 / iPhone 12 Pro Max, natural daylight, leaf on white A4 paper |
| Resolution | Mostly 3024 × 4032 px |
| Format | HEIC (9,815), PNG (1), JPG (1) |
| Processing | None: not cropped, resized, filtered or augmented |
| Curation | 17 duplicates removed (SHA-256 hash and same-leaf check) |
| Split | None provided |

## Classes

| # | Common name | Scientific name | Images |
|---|---|---|---|
| 1 | Amla | *Phyllanthus emblica* | 500 |
| 2 | Jujube | *Ziziphus mauritiana* | 499 |
| 3 | Neem | *Azadirachta indica* | 500 |
| 4 | Wood Apple | *Limonia acidissima* | 499 |
| 5 | Tulsi | *Ocimum tenuiflorum* | 500 |
| 6 | Vasaka | *Justicia adhatoda* | 274 |
| 7 | Moringa | *Moringa oleifera* | 496 |
| 8 | Henna | *Lawsonia inermis* | 498 |
| 9 | Arjun | *Terminalia arjuna* | 497 |
| 10 | Peperomia | *Peperomia* sp. | 502 |
| 11 | Bael | *Aegle marmelos* | 459 |
| 12 | Wild Daisy | *Sphagneticola trilobata* | 507 |
| 13 | Benghal Dayflower | *Commelina benghalensis* | 454 |
| 14 | Licorice Weed | *Scoparia dulcis* | 452 |
| 15 | Mint | *Mentha spicata* | 500 |
| 16 | Buffalo Spinach | *Enydra fluctuans* | 353 |
| 17 | Climbing Hempweed | *Mikania micrantha* | 304 |
| 18 | Bay Leaf | *Cinnamomum tamala* | 394 |
| 19 | Betel Leaf | *Piper betle* | 199 |
| 20 | Guava | *Psidium guajava* | 258 |
| 21 | Lemon | *Citrus* sp. | 355 |
| 22 | Jackfruit | *Artocarpus heterophyllus* | 382 |
| 23 | Java Plum | *Syzygium cumini* | 435 |

## Repository structure

```
MediLeaf23/
├── notebooks/   Colab / Jupyter notebooks (EDA, training, evaluation)
├── src/         Reusable Python code (data loading, models)
├── results/     Metrics, plots and confusion matrices
└── data/        Local copy of the dataset (not uploaded to GitHub)
```

## Getting the data

1. Download the archives from [Mendeley Data](https://doi.org/10.17632/w9nnvf3t6p.1).
2. Extract them into `data/`, giving one folder per class (for example `data/class-01_Amla_Phyllanthus_emblica/`).
3. HEIC images can be opened in Python with `pillow-heif`:

```python
from PIL import Image
from pillow_heif import register_heif_opener

register_heif_opener()
img = Image.open("data/class-01_Amla_Phyllanthus_emblica/IMG_0001.HEIC")
```

## Possible uses

- Training and benchmarking leaf-image classifiers for medicinal plants
- Transfer learning
- Image preprocessing studies
- Testing how sensitive models are to the background

## Citation

If you use MediLeaf-23, please cite:

```bibtex
@dataset{punna2026medileaf23,
  author    = {Punna, Tanjila Tasnim and Bhuiyan, Ashik and Hasan, Md. Firoz and Hoque, Sanzida},
  title     = {MediLeaf-23: Leaf Images of 23 Medicinal Plant Categories Collected in Bangladesh},
  year      = {2026},
  publisher = {Mendeley Data},
  version   = {1},
  doi       = {10.17632/w9nnvf3t6p.1}
}
```

## Contributors

Tanjila Tasnim Punna · Ashik Bhuiyan · Md. Firoz Hasan · Sanzida Hoque

Daffodil International University · Sher-e-Bangla Agricultural University

## License

The dataset is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
