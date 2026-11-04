# Accessible Voice Assistant

A simple Python voice assistant for Windows. It can listen to voice commands, speak replies, open websites, and perform basic tasks.

> **Start with Method 1.** You do not need a virtual environment if the normal installation works. Use Method 2 only if Method 1 does not work.

---

## Before you start

- Install Python on your Windows computer.
- Install [Visual Studio Code](https://code.visualstudio.com/).
- Have a microphone and speakers connected.
- Keep an internet connection available for online speech recognition.

## Method 1 — Run without a virtual environment

### 1. Open the project in VS Code

1. Open VS Code.
2. Select **File → Open Folder**.
3. Select your project folder.
4. Open your Python file. Save it as `ok.py` if you are pasting the code.

### 2. Open the terminal

Select **Terminal → New Terminal** from the top menu.

You can also press **Ctrl + `**.
<img width="1915" height="1010" alt="Screenshot 2026-11-05 000914" src="https://github.com/user-attachments/assets/a71c9e62-162e-43e9-b109-0e7fd4ee9bf4" />


### 3. Install the required packages

Copy this command into the terminal and press Enter:

```bash
python -m pip install SpeechRecognition sounddevice numpy pyttsx3
```

If that does not work, try:

```bash
pip install SpeechRecognition sounddevice numpy pyttsx3
```

If Windows does not recognise `python`, try:

```powershell
py -m pip install SpeechRecognition sounddevice numpy pyttsx3
```

Wait until installation finishes.

### 4. Run the program

```bash
python ok.py
```

Replace `ok.py` with your actual Python filename if different.

> **Done?** If the application opens and works, you can stop here. You do not need a virtual environment.

---

## Method 2 — Use a virtual environment

Use this method only if Method 1 does not work.

### 1. Open Python Environments

1. Find the **Python** icon or **Python Environments** view in the VS Code left sidebar.
2. Open the `venv` section.
3. Click the **+** button.
4. When the menu appears, select **Create Quick**.

![Create a virtual environment](https://github.com/user-attachments/assets/bf7096bb-fded-4048-93f2-3fc00d5bd726)

If you cannot find the Python icon, install the Microsoft Python extension.

You can also press **Ctrl + Shift + P**, search for **Python: Create Environment**, choose **Venv**, and select your Python version.

### 2. Open the terminal

After creating the environment, open the **Terminal** tab.

If it is not visible, select **Terminal → New Terminal**.

![Open terminal after creating environment](https://github.com/user-attachments/assets/4e914093-5a99-4b5f-8ad7-141553715878)

### 3. Install the packages

Run:

```bash
python -m pip install SpeechRecognition sounddevice numpy pyttsx3
```

If that does not work, try:

```bash
pip install SpeechRecognition sounddevice numpy pyttsx3
```

### 4. Run the program

```bash
python ok.py
```

Make sure VS Code is using the newly created `.venv` environment.

---

## Method 3 — Run the Windows EXE file

You can use the pre-built Windows executable without installing Python packages.

**[Download Voice Assistant EXE](https://drive.google.com/file/d/16N_Bt5rWjhmZX5iC_oeZ6m_YnVRzccbe/view)**

1. Open the download link.
2. Download the EXE file.
3. Open the folder where it was downloaded.
4. Double-click the EXE file.

### If Windows shows "Windows protected your PC"

![Windows SmartScreen warning](https://github.com/user-attachments/assets/99de3507-95be-40a7-bae1-05cc70b6df39)

1. Make sure the file is the Voice Assistant EXE you intended to download.
2. Click **More info**.
3. Check the application name.
4. Click **Run anyway**.
5. If a User Account Control prompt appears, click **Yes** only if you trust the file.

**Important:** Google Drive may display a message saying it cannot scan the file for viruses. Download it only if you trust the source. If Windows Security or your browser reports malware, do not bypass that warning. Never turn off Microsoft Defender.

---

## Microphone permission

If voice input does not work, check Windows microphone permissions.

### Windows 11

1. Open **Start → Settings**.
2. Go to **Privacy & security → Microphone**.
3. Turn **Microphone access** ON.
4. Turn **Let apps access your microphone** ON.
5. Turn **Let desktop apps access your microphone** ON.

Desktop applications may not appear individually in the app list. The desktop apps permission is important.

### Windows 10

1. Open **Start → Settings**.
2. Go to **Privacy → Microphone**.
3. Turn on **Allow access to the microphone on this device**.
4. Turn **Allow apps to access your microphone** ON.
5. Turn **Allow desktop apps to access your microphone** ON.

### Check your microphone and speakers

1. Open **Settings → System → Sound**.
2. Under **Input**, select your microphone.
3. Speak and check whether the input level changes.
4. Under **Output**, select your speakers or headphones.
5. Check the volume.

If it still does not work, reconnect your microphone, close other applications using it, and restart the assistant.

For more information, see [Microsoft's microphone permission guide](https://support.microsoft.com/en-us/windows/privacy/turn-on-app-permissions-for-your-microphone-in-windows).

---

## Packages used

- `SpeechRecognition`
- `sounddevice`
- `numpy`
- `pyttsx3`

The project also uses Python built-in modules such as `tkinter`, `threading`, `webbrowser`, `subprocess`, `datetime`, and `platform`.

## Troubleshooting

| Problem | Solution |
|---|---|
| `ModuleNotFoundError` | Install the packages again using the same Python interpreter. |
| Python not recognised | Try `py -m pip` instead of `python -m pip`. |
| Microphone not detected | Check Windows microphone permissions. |
| No sound | Check Windows sound output settings. |
---

*Your VS Code layout may look slightly different depending on the version and installed extensions.*
