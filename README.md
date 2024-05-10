# OLLAMA

OLLAMA is a versatile tool for running and managing large language models (LLMs) locally. It provides an easy-to-use command-line interface for downloading and executing a range of pre-trained models.

## Resources

- [Download OLLAMA](https://ollama.com/)
- [GitHub Repo](https://github.com/ollama/ollama)

## Linux Installation

To install OLLAMA on your Linux system, follow these steps:

1. **Run the Installation Command:**

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

2. **Verify the Installation:**

After the installation completes, check that OLLAMA is installed correctly by running:

```bash
ollama --version
```

You should see the output indicating the version of OLLAMA installed, for example:

```bash
ollama version 0.1.33
```

## Downloading Models

```bash
ollama run <llm_model_name>
```

| Model              | Parameters | Size  | Download                       |
| ------------------ | ---------- | ----- | ------------------------------ |
| Llama 3            | 8B         | 4.7GB | `ollama run llama3`            |
| Llama 3            | 70B        | 40GB  | `ollama run llama3:70b`        |
| Phi-3              | 3.8B       | 2.3GB | `ollama run phi3`              |
| Mistral            | 7B         | 4.1GB | `ollama run mistral`           |
| Neural Chat        | 7B         | 4.1GB | `ollama run neural-chat`       |
| Starling           | 7B         | 4.1GB | `ollama run starling-lm`       |
| Code Llama         | 7B         | 3.8GB | `ollama run codellama`         |
| Llama 2 Uncensored | 7B         | 3.8GB | `ollama run llama2-uncensored` |
| LLaVA              | 7B         | 4.5GB | `ollama run llava`             |
| Gemma              | 2B         | 1.4GB | `ollama run gemma:2b`          |
| Gemma              | 7B         | 4.8GB | `ollama run gemma:7b`          |
| Solar              | 10.7B      | 6.1GB | `ollama run solar`             |

# Open WebUi

Before you can run `open-webui`, you'll need to have Docker and Docker Compose installed on your machine.

## Install Docker

- [Linux](https://docs.docker.com/engine/install/ubuntu/)

## Running the Container

With Docker and Docker Compose installed and your configuration ready, start your open-webui application:

```bash
docker-compose up -d
```

## Accessing Open WebUI

Once the container is running, access Open WebUI through your browser:

```
http://localhost:8686
```

## Optional Configuration: Custom Hostname

If you prefer to access Open WebUI via a custom hostname such as ollama.ai instead of using localhost, follow these steps to update your hosts file:

### Update Hosts File

1. Locate the Hosts File:

   - On Windows, it's located at `C:\Windows\System32\drivers\etc\hosts`.
   - On MacOS and Linux, it's located at `/etc/hosts`.

2. Edit the Hosts File:

   Open the hosts file with administrative (or root) privileges in a text editor:

   - Windows: Open Notepad as Administrator, then open the hosts file.
   - Mac/Linux: Open a terminal and run `sudo nano /etc/hosts`.

3. Add Your Custom Hostname:

   Append the following line to the end of the file. Replace your-machine-ip with the IP address of the machine where Docker is running, which may be `127.0.0.1` if it's the same machine, or another local network IP address if it's different.

4. Save and Close the File:

   - Windows: Save the file and exit Notepad.
   - Mac/Linux: Press CTRL+O to save, then CTRL+X to exit nano.

### Accessing Open WebUI via Custom Hostname

Once the hosts file is updated, you can access `Open WebUI` by navigating to `http://ollama.ai:8686` in your web browser.
