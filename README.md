# AI-Driven Automated Caption Generator

# 1. Aim of the Project
To develop an end-to-end automated pipeline that transcribes video speech and overlays high-quality, synchronized captions. The system aims to provide content creators and educators with a fast, GPU-accelerated tool to enhance video accessibility and engagement without manual editing.

# 2. Abstract
Manual captioning is a time-consuming process that often hinders rapid content distribution. This project introduces an AI-driven solution utilizing OpenAI Whisper for high-accuracy speech-to-text transcription and MoviePy for precise visual synchronization. By leveraging the Transformers library for text processing and running on Google Colab's cloud-based GPUs, the tool transforms raw footage into captioned media instantly, supporting over 50 languages and various video formats.

# 3. Technical Methodology
# 3.1 Speech-to-Text Engine
* Engine: OpenAI Whisper.
* Logic: Extracts the audio stream from the video and processes it through a pre-trained multi-lingual transformer model to generate text with millisecond-accurate timestamps.

# 3.2 NLP and Text Processing
* Framework: Hugging Face Transformers.
* Logic: Used for advanced text segmentation and punctuation correction to ensure captions are readable and aesthetically formatted for small screens (e.g., Shorts/Reels).

# 3.3 Video Rendering and Overlay
* Library: MoviePy.
* Logic: Programmatically generates "TextClip" objects based on timestamps and "burns" them into the video frames. Handles font styling, stroke borders, and positioning.

# 3.4 Infrastructure
* Platform: Google Colab (utilizing NVIDIA T4/A100 GPUs).
* Environment: Python-based execution environment with hardware acceleration enabled for fast FFmpeg rendering.

# 4. Key Performance Results
* Transcription Accuracy: High precision even in noisy background environments due to Whisper's robust architecture.
* Language Support: Automatic language detection and transcription for 50+ languages.
* Processing Speed: Optimized to process a 1-minute video in less than 30 seconds using GPU acceleration.
* Customization: Supports dynamic font sizing, primary/secondary colors, and caption alignment (Bottom/Center/Top).

# 5. Implementation Status
* Development: Python scripts for audio extraction, transcription, and video merging are fully completed.
* Integration: Workflow is integrated into a single-click Google Colab notebook for user convenience.
* Testing: Successfully tested with various video formats (.mp4, .mkv, .mov) and different speaker accents.
* Status: The tool is fully functional and ready for deployment as an open-source captioning utility.

# 6. References
* A. Radford et al., "Robust Speech Recognition via Large-Scale Weak Supervision" (OpenAI Whisper), 2022.
* T. Wolf et al., "Transformers: State-of-the-Art Natural Language Processing," 2020.
* MoviePy Documentation, "Video Editing with Python," 2023.
* Google Colab Hardware Acceleration Guides, 2024.
