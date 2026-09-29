# EduSense Edge: On-Device AI Study Companion

EduSense Edge is a conceptual AI-powered desktop application designed to track student focus, monitor posture, and transcribe offline lectures locally using the **Qualcomm AI Hub** and **Snapdragon NPU**.

## Architecture Intention
This project is architected for Snapdragon-powered Windows PCs. By routing inferencing for Computer Vision (MediaPipe/YOLOv8) and NLP (Whisper) to the NPU, we achieve:
1. **Zero-Latency:** Real-time processing without network calls.
2. **Total Privacy:** Biometric webcam data and audio never leave the device.
3. **Battery Efficiency:** Offloading continuous AI workloads from the CPU/GPU to the Hexagon NPU.

## Codebase Status
The current `app.py` contains the architectural boilerplate for the video capture loop and the integration points where the quantized Qualcomm AI Hub models will be loaded for edge inference.
