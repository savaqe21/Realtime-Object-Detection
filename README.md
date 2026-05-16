# 🖊️ Detekcja Długopisu i Kalkulatora (YOLOv11)

Projekt wykorzystuje model YOLOv11 do rozpoznawania obiektów w czasie rzeczywistym. Wytrenowany lokalnie na Macu M1.

## 🚀 Szybki start (po sklonowaniu)

### 1. Przygotowanie środowiska (Conda)

Jeśli nie masz Condy, zainstaluj [Miniforge](https://github.com/conda-forge/miniforge).

```bash
conda create -n projekt_ai python=3.11 -y
conda activate projekt_ai
pip install ultralytics
```

### 2. Będąc w głównym folderze projektu, wpisz:

```bash
yolo predict model=best.pt source=0 show=true
```

### 3. 📊 Informacje o modelu

• Klasy: dlugopis, kalkulator
• Model: YOLOv11n (Nano)
• Urządzenie: Apple Silicon (MPS)
• Wyniki: mAP50 = 54%
