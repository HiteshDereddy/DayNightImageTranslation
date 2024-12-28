# Round-the-Clock Image Translation

This repository implements a CycleGAN-based approach for converting daytime images to nighttime and vice versa. The project demonstrates unpaired image-to-image translation using deep generative models.

---

## Features
- **Day-to-Night Conversion**: Translates daytime images to nighttime scenes.
- **Night-to-Day Conversion**: Translates nighttime images to daytime scenes.
- **Cycle Consistency**: Ensures the original image can be reconstructed from the translated image.
- **Custom Dataset Support**: Easily train on your own dataset.

---

## Project Structure
```
DayNightImageTranslation/
├── data/                # Dataset (day and night images)
├── models/              # Model architectures and weights
├── scripts/             # Training, evaluation, and utility scripts
├── results/             # Output images and logs
├── README.md            # Project documentation
└── requirements.txt     # Python dependencies
```

---

## Getting Started

### Prerequisites
- Python 3.8 or later
- GPU with CUDA support (optional but recommended)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/DayNightImageTranslation.git
   cd DayNightImageTranslation
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Prepare your dataset:
   Organize your images into `data/day` and `data/night` directories.

---

## Training

1. **Train the CycleGAN model**:
   ```bash
   python scripts/train.py --dataset_path ./data --epochs 100
   ```

2. **Monitor training**:
   Use TensorBoard to visualize training progress:
   ```bash
   tensorboard --logdir=results/logs
   ```

---

## Evaluation

1. **Generate translations**:
   ```bash
   python scripts/test.py --input ./data/day/test --output ./results/night
   ```

2. **View results**:
   Check the `results/` directory for translated images.

---

## Example Results

| Input (Day) | Output (Night) |
|-------------|----------------|
| ![Day](results/sample_day.jpg) | ![Night](results/sample_night.jpg) |

---

## Acknowledgments
This project leverages the [CycleGAN](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix) framework for unpaired image-to-image translation.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Contact
For questions or feedback, contact [your-email@example.com].
