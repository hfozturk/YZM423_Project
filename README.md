# 🏛️ Legal AI - Hukuki Risk Analizi

Türkçe sözleşme metinlerindeki hukuki riskleri otomatik olarak tespit eden ve sınıflandıran yapay zeka projesi.

![Python](https://img.shields.io/badge/Python-3.12-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.9-red)
![Transformers](https://img.shields.io/badge/Transformers-4.57-orange)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📋 Proje Hakkında

Bu proje, **Mistral-7B** büyük dil modelini **LoRA (Low-Rank Adaptation)** yöntemiyle fine-tune ederek Türkçe hukuki sözleşmelerdeki riskleri analiz eden bir sistem geliştirmeyi amaçlamaktadır.

### ✨ Özellikler

- 🔍 Türkçe sözleşme maddelerinde otomatik risk tespiti
- 📊 Risk seviyesi sınıflandırması (DÜŞÜK / ORTA / YÜKSEK)
- 🏷️ Risk türü belirleme (Tek Taraflı Fesih, Rekabet Yasağı, Sorumsuzluk Kaydı vb.)
- 💡 Detaylı risk açıklaması üretimi
- ⚡ 4-bit quantization ile verimli bellek kullanımı

---

## 🛠️ Kullanılan Teknolojiler

| Teknoloji | Versiyon | Açıklama |
|-----------|----------|----------|
| **Mistral-7B** | v0.1 | Temel dil modeli |
| **LoRA/PEFT** | 0.18+ | Verimli fine-tuning |
| **BitsAndBytes** | 0.49+ | 4-bit quantization |
| **Transformers** | 4.57+ | Model framework |
| **TRL** | 0.26+ | Training kütüphanesi |

---

## 📁 Proje Yapısı

```
├── YZM-423_220212002_LegalAi.ipynb   # Ana notebook dosyası
└── README.md                          # Bu dosya
```

---

## 🚀 Kurulum ve Çalıştırma

### Google Colab'da Çalıştırma (Önerilen)

1. Notebook'u Google Colab'a yükleyin
2. Runtime → Change runtime type → **T4 GPU** seçin
3. Hücreleri sırasıyla çalıştırın

### Gerekli Kütüphaneler

```bash
pip install -U transformers datasets accelerate bitsandbytes trl peft
```

---

## 📊 Model Özellikleri

| Özellik | Değer |
|---------|-------|
| Base Model | Mistral-7B-v0.1 |
| Eğitilebilir Parametre | 3.4M (%0.047) |
| Quantization | 4-bit NF4 |
| LoRA Rank | 8 |
| Training Steps | 60 |
| Final Loss | 0.93 |

---

## 💻 Kullanım Örneği

```python
# Sözleşme maddesi analizi
prompt = """### Instruction:
Aşağıdaki sözleşme maddesini analiz et ve olası hukuki riskleri belirle.

### Input:
Kiralayan, herhangi bir sebep göstermeksizin sözleşmeyi tek taraflı olarak feshedebilir.

### Response:
"""

# Model çıktısı
# Risk Seviyesi: YÜKSEK
# Risk Türü: Tek Taraflı Fesih Hakkı
# Açıklama: Bu madde kiracı açısından ciddi hukuki risk taşır...
```

---

## 📈 Eğitim Sonuçları

- ✅ Training Loss: 0.93 (başarılı konverjans)
- ✅ Eğitim Süresi: ~5 dakika
- ✅ Bellek Kullanımı: ~4GB (4-bit quantization)

---

## 🎯 Kullanım Alanları

- 📄 Kira sözleşmesi risk analizi
- 💼 İş sözleşmesi incelemesi
- 🛒 Satış sözleşmesi kontrolü
- ⚖️ Hukuki belge değerlendirmesi

---

## 👨‍💻 Geliştirici

**Öğrenci No:** 220212002  
**Ders:** YZM-423

---

## 📝 Lisans

Bu proje eğitim amaçlı geliştirilmiştir.

---

## 🙏 Teşekkürler

- [Mistral AI](https://mistral.ai/) - Base model
- [Hugging Face](https://huggingface.co/) - Transformers ekosistemi
- [Google Colab](https://colab.research.google.com/) - GPU kaynakları

