# NCOS

# Get Started

Dieses Repository beinhaltet die Logik, um Noxtua NCOS auszuführen. Zum schnellen Testen mit einem Chat wird eine Gradio Anwendung verwendet.

## Voraussetzungen

1. Installiere Docker and Python (getestet mit Version 3.11.2)
2. Ausführen von Vllm

    ```sh
    docker run --runtime nvidia --gpus all -v ~/.cache/huggingface:/root/.cache/huggingface -p 8000:8000 --ipc=host vllm/vllm-openai:v0.6.6.post1 --model  --tensor-parallel-size=2 --disable-log-requests --max-model-len 120000 --gpu-memory-utilization 0.95
    ```

## Setup

```sh
pip install -r requirements.txt
```

## Gradio Anwendung

```sh
python app.py
```

Dieser Befehl startet die Gradio Anwendung mit einem Chat im localhost unter dem angegebenen Port `8015`. Zum Aufrufen den angezeigten Link im Browser öffnen z.b. "http://0.0.0.0:8015" oder "http://localhost:8015".