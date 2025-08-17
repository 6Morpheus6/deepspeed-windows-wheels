# DeepSpeed Windows Wheels with RTX 50 Support

Prebuilt **DeepSpeed** wheels for **Windows** with **NVIDIA GPU support**.  
Supports **Python 3.9 – 3.12** and **GTX 10** - **RTX 50** series.
Compiled with **pytorch 2.7, 2.8 and cuda 128**  
> “The wheels already include CUDA 12.8 support – no separate CUDA toolkit installation  required.”

---

## 📜 Notes

These wheels are provided to simplify DeepSpeed installation on Windows without manual building.  
Official DeepSpeed repository: [https://github.com/deepspeedai/DeepSpeed](https://github.com/deepspeedai/DeepSpeed)

> ⚠ **Windows Notice**  
You may see warnings like:  
`LINK : fatal error LNK1181: cannot open file "aio.lib"`  
`LINK : fatal error LNK1181: cannot open file 'cufile.lib'`  
This is normal on systems without the full CUDA Toolkit.  
DeepSpeed will still work for all regular training and inference tasks.

---

## 🖥️ Requirements

- Windows 10 / 11 (x64)  
- NVIDIA GPU with CUDA-capable drivers  
- Python 3.9 – 3.12  
- pip >= 21.0

---

## 🔧 Preparation

- 1.) **Create Project**
  - Create new folder: `mkdir MyProject`
  - Navigate to new folder: `cd MyProject`
  - Optional install uv: `conda install -y -c conda-forge uv`
- 2.) **Python Environment**
  - Create Environment: `python -m venv env`
  - Activate Environment: `env\Scripts\activate`
- 3.) **Pytorch 2.7.x+cu128 or 2.8.x+cu128**
  - Install pytorch 2.7.0, pytorch 2.7.1 or pytorch 2.8.0 with pip:
  
    **pytorch 2.7.0**

    ```bash
    pip install torch==2.7.0 torchvision==0.22.0 torchaudio==2.7.0 --index-url https://download.pytorch.org/whl/cu128
    ```

    **pytorch 2.7.1**

    ```bash
    pip install torch==2.7.1 torchvision==0.22.1 torchaudio==2.7.1 --index-url https://download.pytorch.org/whl/cu128
    ```

    **pytorch 2.8.0**

    ```bash
    pip install torch==2.8.0 torchvision==0.23.0 torchaudio==2.8.0 --index-url https://download.pytorch.org/whl/cu128
    ```

  - Or install with uv:
  
    **pytorch 2.7.0**

    ```bash
    uv pip install torch==2.7.0 torchvision==0.22.0 torchaudio==2.7.0 --index-url https://download.pytorch.org/whl/cu128
    ```

    **pytorch 2.7.1**

    ```bash
    uv pip install torch==2.7.1 torchvision==0.22.1 torchaudio==2.7.1 --index-url https://download.pytorch.org/whl/cu128
    ```

    **pytorch 2.8.0**

    ```bash
    uv pip install torch==2.8.0 torchvision==0.23.0 torchaudio==2.8.0 --index-url https://download.pytorch.org/whl/cu128
    ```

---

## 📦 Installation

Search the appropriate `.whl` file for your pytorch and python version from the [Releases](https://github.com/6Morpheus6/deepspeed-windows-wheels/releases) page.

### Install it with pip

```bash
pip install https://github.com/6Morpheus6/deepspeed-windows-wheels/releases/download/<tag>deepspeed‑<version>‑<torch version>torch+cu128-cp<python version>‑cp<python version>‑win_amd64.whl
```

**For Example:**

```bash
pip install https://github.com/6Morpheus6/deepspeed-windows-wheels/releases/download/v0.17.5/deepspeed-0.17.5+e1560d84-2.7torch+cu128-cp310-cp310-win_amd64.whl
```

### Or install with uv

```bash
uv pip install https://github.com/6Morpheus6/deepspeed-windows-wheels/releases/download/<tag>deepspeed‑<version>‑<torch version>torch+cu128-cp<python version>‑cp<python version>‑win_amd64.whl
```

**For Example:**

```bash
uv pip install https://github.com/6Morpheus6/deepspeed-windows-wheels/releases/download/v0.17.5/deepspeed-0.17.5+e1560d84-2.7torch+cu128-cp310-cp310-win_amd64.whl
```

### ⭐ Support

If this project is useful to you, please consider giving it a ⭐ on GitHub!
