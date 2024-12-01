# CycleTrans: Unpaired Language Translation with Adversarial and Cycle Consistency

CycleTrans is an advanced model for **unpaired language translation**, using **adversarial training** and **cycle consistency** to translate between languages without requiring parallel datasets. This model allows seamless translation between languages such as **English** and **Italian** using two separate, unaligned datasets.

## 🚀 Overview
CycleTrans is built to work with unpaired datasets—meaning you don't need exact translations for each sentence. It uses **two generators** and **two discriminators** inspired by **Generative Adversarial Networks (GANs)** to ensure high-quality translations. The model also incorporates **cycle consistency** to maintain translation accuracy between languages.

### Key Features:
- **Unpaired Data**: Train the model with two separate datasets (e.g., English and Italian).
- **Adversarial Training**: The generators produce translations while the discriminators help improve their quality.
- **Cycle Consistency**: Ensures that translating between languages in both directions yields the same original sentence.
- **Contrastive Loss**: Aligns sentences in the shared embedding space for better translation quality.

## 🧠 How It Works

CycleTrans architecture consists of:
1. **Shared Embedding Layer**: A shared embedding that maps both English and Italian sentences into the same representation space.
2. **Two Generators**:
   - **G_E2I (English to Italian)**: Translates from English to Italian.
   - **G_I2E (Italian to English)**: Translates from Italian to English.
3. **Two Discriminators**:
   - **D_E (English Discriminator)**: Ensures realistic English translations.
   - **D_I (Italian Discriminator)**: Ensures realistic Italian translations.
4. **Cycle Consistency**: Ensures that translated sentences, when converted back to the original language, remain close to the initial sentence.
5. **Adversarial and Contrastive Losses**: Improve the quality of translations by leveraging adversarial training and sentence alignment.

## 💻 Getting Started

### Prerequisites:
- Python 3.x
- PyTorch
- Hugging Face Transformers
- Google Colab or Jupyter Notebook (for easy use)

### Installation:

Clone the repository:
```bash
git clone https://github.com/yourusername/CycleTrans.git
cd CycleTrans
