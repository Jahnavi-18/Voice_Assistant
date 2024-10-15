# Voice_Assistant
This Python script implements a personal voice assistant using the speech_recognition, pyttsx3, and pywhatkit libraries. It can listen for user commands, process them, and respond with appropriate actions like playing songs on YouTube, providing jokes, or opening websites (e.g., Google, Spotify, Netflix). 
Here’s a detailed analysis of the script along with instructions you can include in the `README.md` file for your GitHub repository.

### **Script Overview:**

This Python script creates a voice assistant named "Rolex." It leverages various external libraries and modules to perform actions based on voice commands, such as opening websites, providing jokes, telling the current time, and searching Wikipedia. Below is a structured breakdown of the key components and features, followed by instructions on how to run it.

---

### **Features:**

1. **Speech Recognition**: 
   - Uses `speech_recognition` library to capture and understand voice commands.
   
2. **Text-to-Speech**: 
   - Implements the `pyttsx3` library for voice output to respond to the user.
   
3. **Control over External Applications**:
   - Opens Google Chrome, Spotify, WhatsApp Web, YouTube, Google Maps, Netflix, Prime Video, LinkedIn, and more based on specific voice commands.
   
4. **Media Control**:
   - Uses `pywhatkit` to play YouTube songs based on user requests.
   
5. **Wikipedia Integration**:
   - Retrieves brief summaries from Wikipedia when asked about a person.

6. **Miscellaneous**:
   - Tells the time, cracks jokes using `pyjokes`, and offers a variety of personalized responses.

### **Requirements**:

The script depends on the following libraries:

- `speech_recognition`: For capturing and processing voice input.
- `pyttsx3`: For text-to-speech conversion.
- `pywhatkit`: For playing YouTube videos via voice commands.
- `wikipedia`: For fetching information from Wikipedia.
- `pyjokes`: To provide jokes.
- `webbrowser`: To open specific websites based on commands.
- `subprocess`: To launch local applications (e.g., Google Chrome).

### **Installation**:

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/yourusername/rolex-voice-assistant.git
   cd rolex-voice-assistant
   ```

2. Install the required dependencies:
   ```bash
   pip install speechrecognition pyttsx3 pywhatkit wikipedia pyjokes
   ```

3. Ensure you have an active microphone and internet connection.

### **How to Run**:

1. **Run the script**:
   ```bash
   python rolexpy.py
   ```

2. The assistant will listen for commands and execute them. Some of the available commands include:
   
   - **Playing a song**:  
     - Say: "Play [song name]"  
     Example: "Play Shape of You"  
     (This command plays the requested song on YouTube.)
   
   - **Getting information from Wikipedia**:  
     - Say: "Who is [person's name]"  
     Example: "Who is Albert Einstein"
   
   - **Checking the time**:  
     - Say: "What time is it?"
   
   - **Telling a joke**:  
     - Say: "Tell me a joke"
   
   - **Opening websites**:  
     - Say: "Open Google", "Open Spotify", "Open Netflix", "Open WhatsApp", etc.

3. The assistant will respond verbally to your command or take the requested action, such as playing music, fetching information from Wikipedia, or opening a browser.

### **Custom Commands**:

You can modify the script to add more commands by updating the `run_rolex()` function. Add new `elif` conditions to handle specific commands. Example:

```python
elif 'news' in command:
    talk('Fetching the latest news')
    webbrowser.open('https://news.google.com')
```

### **Important Notes**:

- This script is designed for personal use and can be customized easily to fit more functionality.
- Ensure that your microphone is properly set up and recognized by the system before running the script.
- The script currently runs indefinitely in a `while` loop. You can stop it using a keyboard interrupt (`Ctrl+C`).

---

### Example `README.md` File

```markdown
# Rolex Voice Assistant

Rolex is a Python-based voice assistant that listens to user commands and performs actions like playing YouTube videos, fetching information from Wikipedia, cracking jokes, and opening websites. It's powered by popular Python libraries such as `speech_recognition`, `pyttsx3`, and `pywhatkit`.

## Features

- **Voice recognition**: Listens to user commands and interprets them.
- **Text-to-Speech**: Responds using speech output.
- **Search Wikipedia**: Retrieves information based on voice commands.
- **Play YouTube songs**: Plays requested songs using YouTube.
- **Open websites**: Opens common websites such as Google, Spotify, YouTube, Netflix, etc.
- **Tell jokes**: Provides jokes using the `pyjokes` library.
- **Tell the time**: Responds with the current time.

## Requirements

- `speechrecognition`
- `pyttsx3`
- `pywhatkit`
- `wikipedia`
- `pyjokes`

Install them using the following command:

```bash
pip install speechrecognition pyttsx3 pywhatkit wikipedia pyjokes
```

## Usage

To start the Rolex Voice Assistant, run the script:

```bash
python rolexpy.py
```

### Available Commands

- **Play [song name]**: Plays the requested song on YouTube.
- **Who is [person's name]**: Fetches information from Wikipedia.
- **What time is it**: Tells the current time.
- **Tell me a joke**: Tells a joke using `pyjokes`.
- **Open [website]**: Opens websites like Google, Spotify, Netflix, etc.

## Customization

You can add more voice commands by editing the `run_rolex()` function.

Example:
```python
elif 'news' in command:
    talk('Fetching the latest news')
    webbrowser.open('https://news.google.com')
```

## License

This project is licensed under the MIT License.
```

This README provides clear instructions on how to install, run, and customize the assistant.
