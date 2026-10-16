# Workplace Safety Sentinel — CraftifAI PipeGen

A real-time physical AI vision pipeline built with CraftifAI PipeGen (Track A) to monitor industrial hazard zones and trigger alerts on unauthorized worker intrusion.

---

## 📌 Problem Statement
Industrial facilities and heavy machinery workspaces face severe risks when personnel wander into restricted zones undetected. Manual monitoring often leads to delayed reactions and workplace incidents.

---

## 💡 Solution Overview
Workplace Safety Sentinel ingests video streams and detects workers using an edge-optimized YOLOv8 model compiled into a high-performance TensorRT FP16 engine. Boundary polygon calculations identify restricted perimeter breaches and broadcast real-time JSON alert streams to facility MQTT brokers.

---

## 🏗️ Pipeline Architecture
`Video Stream (MP4/RTSP)` ➔ `Pre-processing (Resize 640x640, Normalization)` ➔ `TensorRT FP16 Inference Engine` ➔ `Perimeter / Hazard Zone Analytics` ➔ `Actionable Sink (JSON / MQTT Broadcast)`

---

## ⚡ TensorRT Benchmark Report (Tesla T4)
- **Engine Type**: TensorRT FP16 (Half Precision)
- **Input Resolution**: 640x640
- **Average Inference Latency**: 7.88 ms
- **Throughput**: 126.8 FPS
- **GPU Memory Allocated**: 7.38 MB
- **Target Platform**: NVIDIA Cloud / Jetson Edge Target

---

## 🚀 Quickstart
```bash
chmod +x run.sh
./run.sh
