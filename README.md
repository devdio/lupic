# Lupic Practice

🌐 **English** | [한국어](README.ko.md)

Learning materials for controlling the Kamibot educational robot with Python and an LLM (AI).
This guide is organized in **Install → Practice** order so that even first-timers can follow along.

Follow the steps in order.

1. [Install the USB dongle driver](#step-1-install-the-usb-dongle-driver)
2. [Install JupyterLab Desktop](#step-2-install-jupyterlab-desktop)
3. [Run the practicals (01 ~ 05)](#step-3-run-the-practicals-01--05)

---

## Step 1. Install the USB dongle driver

Kamibot connects to your PC through a USB dongle (a wireless communication device).
You must **install the driver first** so that your PC can recognize the dongle.

### How to install

1. Run the installer included in this repository.  [DOWNLOAD Dongle Driver](https://github.com/devdio/lupic/raw/main/CDM21228_Setup.exe)

2. When the wizard appears, proceed in order: **Extract → Next → Accept the agreement → Finish**.
3. After installation, plug the USB dongle into your PC.

> 💡 If you do not install the driver, practical 01 will fail to find the dongle (port).
> Be sure to finish this step first.

---

## Step 2. Install JupyterLab Desktop

The practicals are run as **Jupyter notebooks (`.ipynb`)**.
To run these notebooks, install **JupyterLab Desktop**.

### How to install

1. Go to the download page below.

   👉 https://github.com/jupyterlab/jupyterlab-desktop/releases

2. From the latest version (Latest) at the top, download the installer for your operating system.

   - **Windows**: `JupyterLab-Setup-Windows-x64.exe`
   - **macOS**: `JupyterLab-Setup-macOS-...dmg`
   - **Linux**: `.deb` or `.AppImage`

3. Run the downloaded file and install it by following the instructions.
4. After installation, launch **JupyterLab Desktop**.

### Opening the practice files

1. In the JupyterLab Desktop screen, open this project folder (`lupic`).
2. In the file list on the left, double-click a practice notebook (e.g. `01_KAMIBOT_en.ipynb`) to open it.

> 💡 To run a code cell in a notebook, click the cell and press **Shift + Enter**.

---

## Step 3. Run the practicals (01 ~ 05)

Proceed in the order below. Each notebook contains the library installation steps and examples it needs.

| Order | File | Contents |
|-------|------|----------|
| 01 | [01_KAMIBOT_en.ipynb](01_KAMIBOT_en.ipynb) | **Kamibot basic control** — install the Python library (`pykamilab`), find the connection port, and move the robot |
| 02 | [02_AGENT_en.ipynb](02_AGENT_en.ipynb) | **Intro to LangChain agents** — build the simplest AI agent with the latest LangChain `create_agent` |
| 03 | [03_LANGGRAPH_en.ipynb](03_LANGGRAPH_en.ipynb) | **Intro to LangGraph** — build the same agent in a graph (nodes & edges) style and control the flow yourself |
| 04 | [04_LLMtoROBOT_en.ipynb](04_LLMtoROBOT_en.ipynb) | **Control the robot with an LLM** — build an agent that understands natural-language commands to move Kamibot |
| 05 | [05_RSLtoROBOT_en.ipynb](05_RSLtoROBOT_en.ipynb) | **Control the robot with RSL** — have the LLM generate a robot-specific language (RSL), then validate and run it to drive the robot |

### Tips for proceeding

- Run the code cells in a notebook **from top to bottom in order**.
- Practical 01 requires the robot and dongle to be connected to your PC.
- Practicals 02 ~ 05 require an LLM API key (e.g. OpenAI or Anthropic).
  Follow the instructions in each notebook to prepare your API key.

---

## Requirements summary

- A Kamibot robot unit and its USB dongle
- A Windows / macOS / Linux PC
- An LLM API key (used in practicals 02 ~ 05)

## API Key
```
import os
os.environ["OPENAI_API_KEY"] = "sk-..."

print(os.environ.get("OPENAI_API_KEY"))
```

## Reference links

- JupyterLab Desktop download: https://github.com/jupyterlab/jupyterlab-desktop/releases
- pykamilab (Kamibot Python library): https://pypi.org/project/pykamilab/
- pykamirsl (RSL library): https://pypi.org/project/pykamirsl/
