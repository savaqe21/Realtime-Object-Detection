# 🖊️ YOLOv11 Object Detection on Apple Silicon (M1)

Projekt akademicki realizujący wykrywanie obiektów codziennego użytku (`dlugopis`, `kalkulator`) w czasie rzeczywistym przy użyciu najnowszej architektury **YOLOv11** (wersja Nano).

Cały proces - od akwizycji danych, przez adnotację w Label Studio, aż po trening sieci neuronowej - został przeprowadzony lokalnie na procesorze **Apple M1** z wykorzystaniem akceleracji graficznej **MPS (Metal Performance Shaders)**.

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

### 3. 📊 Specyfikacja projektu

- **Architektura:** YOLOv11n (101 warstw, ~2.5M parametrów)
- **Zbiór danych:** 127 autorskich zdjęć (podział train/val: 80/20)
- **Czas treningu:** ~11 minut (50 epok na Apple M1 GPU)
- **Uzyskana skuteczność:** mAP50 = 54.1% (kalkulator: 64.4%, długopis: 43.9%)
- **Wydajność detekcji live:** ~34 ms / klatkę (~30 FPS)
