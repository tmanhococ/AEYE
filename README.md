# AEyePro

AEyePro is an educational project that provides a local, standalone health monitoring application with an integrated chatbot assistant. It is designed for learning purposes and is not intended for commercial use.

## 🚀 Features

1. **Posture & Eye Monitoring** (`core/`)

   * Real-time tracking of sitting posture and eye metrics.
   * Calculates indicators such as blink rate, head tilt, shoulder angle, and drowsiness count.

2. **AI Agents** (`models/`)

   * **RAG-Agent**: Retrieval-Augmented Generation for answering health-related queries based on collected data.
   * **Recommend-Agent**: Provides personalized health recommendations.
   * **Submodels**: Includes LLaMA 3.2 3B Instruct Quantized (Q8\_0) model in `models/Submodel/`.

3. **Data Visualization**

   * Interactive charts and graphs to visualize collected posture and eye-tracking metrics.

## 📁 Folder Structure

```
AEyePro/
├── core/                  # Source code for posture & eye monitoring
│   ├── camera.py
│   ├── metrics.py
│   └── utils.py
├── models/                # AI agent implementations and models
│   ├── retrieval_agent.py
│   ├── recommend_agent.py
│   └── Submodel/          # LLaMA model files
│       └── Llama-3.2-3B-Instruct-Q8_0.gguf
├── visualization/         # Scripts for data visualization
│   ├── plot_metrics.py
│   └── dashboard.py
├── GUI/                   # GUI interface modules
│   └── main_ui.py
├── requirements.txt       # Project dependencies
├── README.md              # This file
└── main.py                # Entry point
```

## 💻 Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/AEyePro.git
   cd AEyePro
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   # Windows (PowerShell)
   .\.venv\Scripts\Activate.ps1
   # macOS/Linux
   source .venv/bin/activate
   ```

3. Install dependencies:

   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

4. Ensure your CUDA environment is set up if using GPU for LLaMA:

   * CUDA Toolkit 12.x
   * NVIDIA drivers for RTX 3050 Ti
5. Install:
 https://huggingface.co/bartowski/Llama-3.2-3B-Instruct-GGUF/blob/main/Llama-3.2-3B-Instruct-Q8_0.gguf

## ▶️ Usage

1. **Run the monitoring & visualization GUI**:

   ```bash
   python main.py
   ```

2. **Interact with the chatbot assistant**:

   * Open the chat panel in the GUI.
   * Ask health-related questions based on your posture and eye-tracking data.

3. **Inspect visualized metrics**:

   * Navigate to the Data Visualization tab.
   * View real-time plots of your posture and blink statistics.

## 🤝 Contributing

This project is for educational use. Contributions are welcome:

1. Fork the repo.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m "Add feature"`.
4. Push to branch: `git push origin feature-name`.
5. Open a Pull Request.

## 📄 License

This project is released under the MIT License. See [LICENSE](LICENSE) for details.
