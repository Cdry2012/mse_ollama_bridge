# MSE Ollama Bridge

A simple Google Colab setup to run Ollama, store models in Google Drive, and expose Ollama through a public ngrok URL.

## Steps

### 1. Install Ollama

Install the required package and Ollama:

```bash
!apt-get update -qq && apt-get install -y zstd
!curl -fsSL https://ollama.com/install.sh | sh
```


### 2. Start Ollama

The notebook automatically starts Ollama and checks if the API is ready.

If everything works, you will see:

```text
Ready True
```

### 3. Download the Model

Download the model:

```bash
!ollama pull llama3.1:8b
```

### 4. Install pyngrok

Install the package used to create the public tunnel:

```bash
!pip install pyngrok -q
```

### 5. Create the Public URL

Add your own ngrok authentication token, then run the final cell.

The notebook connects ngrok to Ollama on port `11434` and prints a public URL:

```text
link: https://xxxx.ngrok-free.app
```

Use this URL to access your Ollama server.


## Usage

Run the cells **from top to bottom** in Google Colab.
