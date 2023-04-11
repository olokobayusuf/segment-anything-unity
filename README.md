# Segment Anything in Unity
This is a realtime implementation of Meta AI's [Segment Anything Model](https://ai.facebook.com/blog/segment-anything-foundation-model-image-segmentation) in Unity Engine using NatML.

## How it Works
The SAM projects consists of two models:
1. A large image embedding model
2. A lightweight mask decoder network

We setup the embedding model using a NatML endpoint (see [embedding.ipynb](Endpoints/embedding.ipynb)). We export the lightweight mask decoder network to ONNX, then use NatML to convert it to CoreML for iOS; ONNX for Windows and the web; and TensorFlow Lite for Android.

## Requirements
- NatML 1.1.4+

## Supported Platforms
- Android 24+
- iOS 14+
- macOS 10.15+
- Windows 10+ (64-bit only)
- Web:
    - Chrome 91+
    - Firefox 90+
    - Safari 16.4+