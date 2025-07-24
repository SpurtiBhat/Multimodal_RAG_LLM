# Multimodal_RAG_LLM

Local Multimodal AI Chat is a unified chat application that leverages advanced AI models to handle audio, images, and PDF documents seamlessly. It integrates Whisper AI for audio, LLaVA for image understanding, and Chroma DB for document management — all within a single interface.

Enhanced with the Ollama server and OpenAI API, the app delivers strong performance and flexibility. The project is actively maintained and open to contributions, whether it’s adding new features, improving performance, or fixing bugs. It serves as a practical resource for anyone exploring multimodal AI solutions.

### Features
**Local Model Inference with Ollama**: Run AI models locally using the Ollama server for a fast, secure, and fully customizable experience — eliminating the need for external cloud services. This setup ensures data privacy while significantly reducing latency.

**Seamless OpenAI API Integration**: For extended functionality, the app integrates with the OpenAI API, offering access to powerful hosted models. This hybrid approach combines local performance with the versatility of cloud-based AI, enabling advanced and responsive interactions.

**Voice Chat with Whisper AI**: Powered by OpenAI's Whisper, the app supports natural and accurate voice-based conversations. Whisper enables real-time speech-to-text transcription, making audio interaction smooth and intuitive.

**PDF Interaction via Chroma DB**: Engage with your PDF files like never before. By integrating Chroma DB as a local vector database, the app allows users to extract insights, ask questions, and summarize content from their PDFs — all while maintaining full offline control.

### Complete Manual Install

1. **Install Ollama**

2. **Create a Virtual Environment**

3. **Install Requirements**:
   - ```pip install --upgrade pip```
   - ```pip install -r requirements.txt```
   - ```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu```   

4. **Enter commands in terminal**: 
   1. ```python3 database_operations.py``` This will initialize the sqlite database for the chat sessions.
   2. ```streamlit run app.py```

5. **Pull Models**: Go to https://ollama.com/library and choose the models you want to use. Enter ```/pull MODEL_NAME``` in the chat bar. 
You need one embedding model e.g. [nomic-embed-text](https://ollama.com/library/nomic-embed-text) to embed pdf files and one model which undertands 
images e.g. [llava](https://ollama.com/library/llava) 

6. **Optional**: 
   - Check the config.yaml file and change accordingly to your needs.
   - Place your user_image.png and/or bot_image.png inside the chat_icons folder and remove the old ones. 
