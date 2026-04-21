# 2025 Automatic Meme Generation with Text Based on Facial Expressions

This project combines computer vision and natural language processing to automatically detect facial emotions and generate trendy meme captions. It uses multi-model fusion for robust emotion recognition and integrates a large language model (DeepSeek-Chat) for creative caption generation.

## Features

- Multi-model emotion detection (FER + DeepFace: VGG-Face, FaceNet, OpenFace)
- Emotion fusion and conflict resolution (positive/negative/neutral grouping)
- Dynamic retry and historical data reuse for robustness
- LLM-based caption generation with internet slang style
- Intelligent meme layout and text rendering (auto text region selection, contrast color calculation, adaptive font rendering)

## System Architecture

The system consists of three core modules:

1. **Emotion Detection & Fusion** – Primary (FER) and secondary (DeepFace) detectors with weighted fusion.
2. **Conflict Resolution** – Group-based conflict detection and accumulation strategy.
3. **Caption Generation** – Prompt construction and DeepSeek-Chat API call.

## Results

| Module | Metric | Result |
|--------|--------|--------|
| Emotion Recognition | Accuracy (fusion) | **91%** (FER: 82%, DeepFace: 85%) |
| Caption Generation | Relevance score (1-5) | **4.2** |
| Efficiency | Detection + Caption | ~0.8 sec per image |

### Sample Outputs

- Detected `happy (80%)` → Caption: `超开心`
- Detected `surprise (60%) + fear (30%)` → Caption: `吓一跳`

## Code & Demo

[https://github.com/1234567890244/ECE4513_Final_Project](https://github.com/1234567890244/ECE4513_Final_Project)

## Authors

- **Ruiqi Zhang** – Core algorithm design, system integration, API connectivity
- **Yutian Dai** – Dataset construction, experimentation, statistical analysis, report writing

## License

Please refer to the repository for license information.
