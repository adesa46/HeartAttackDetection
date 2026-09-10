# Heart Attack Detection System

A real-time cardiac monitoring and heart attack detection system using a 6-lead ECG wearable device integrated with Arduino hardware and machine learning models for instant health analysis.

## 📋 Overview
 
This project implements an intelligent wearable ECG monitoring device that:
- **Captures real-time ECG signals** via a 6-lead electrode configuration
- **Detects potential cardiac anomalies** using advanced machine learning models
- **Provides live tracking** of heart rate and ECG patterns
- **Records and analyzes** cardiac data for later review
- **Connects users with healthcare professionals** instantly when needed
- **Manages device operations** including Bluetooth pairing, battery monitoring, and system diagnostics

## 🎯 Key Features

### Live Tracking
- Real-time ECG signal acquisition and visualization
- Continuous heart rate monitoring
- Instant anomaly detection
- Live streaming of cardiac data to the mobile app

### Recording Analysis
- Automatic ECG recording storage
- Post-recording analysis and interpretation
- Historical data tracking
- Detailed cardiac event reports

### App Features
- **Quick Contact**: One-tap connection to emergency contacts and healthcare professionals
- **Battery Management**: Low battery alerts and remaining usage estimates
- **Bluetooth Connectivity**: Seamless device pairing and connection management
- **Device Diagnostics**: System health checks and electrode contact verification
- **Alert System**: Critical event notifications
- **Health Dashboard**: Summary of cardiac metrics and trends

## 🏗️ Project Architecture

```
HeartAttackDetection/
├── models/                     # Machine Learning Models
│   ├── cnn/                   # Convolutional Neural Network
│   ├── lstm/                  # Long Short-Term Memory
│   └── rnn/                   # Recurrent Neural Network
├── Live-Tracking/             # Real-time ECG monitoring
├── Recorded-Tracking/         # ECG analysis & historical data
├── App-Features/              # Mobile app functionality
│   ├── Emergency Contact
│   ├── Battery Management
│   ├── Bluetooth Pairing
│   └── Device Diagnostics
└── test-demo/                 # Testing & Demonstration
```

## 🔌 Hardware Specifications

### Arduino-Based ECG Front-End
- **Microcontroller**: Arduino (signal processing & data transmission)
- **ECG Lead Configuration**: 6-lead system
  - Enhanced cardiac coverage compared to single-lead systems
  - Improved detection sensitivity for cardiac anomalies
  - Multi-directional heart activity monitoring

### Key Hardware Components
- 6-channel analog-to-digital converter (ADC)
- Signal conditioning and amplification circuits
- Bluetooth module for wireless communication
- Power management system with battery monitoring
- Electrode interface connectors

## 🤖 ML Models

The system employs three deep learning architectures for robust cardiac analysis:

### 1. **CNN (Convolutional Neural Network)**
- Pattern recognition in ECG waveforms
- Spatial feature extraction
- Efficient real-time inference

### 2. **LSTM (Long Short-Term Memory)**
- Temporal sequence analysis
- Time-dependent pattern recognition
- Prediction of cardiac events

### 3. **RNN (Recurrent Neural Network)**
- Sequential ECG data processing
- Dynamic pattern modeling
- Adaptive learning from new data

## 🚀 Getting Started

### Prerequisites
- Arduino IDE or compatible development environment
- Python 3.8+
- Required Python libraries (see `requirements.txt` if available):
  - TensorFlow / PyTorch (for ML models)
  - Pandas, NumPy (data processing)
  - Scikit-learn (signal processing)
  - Flask/FastAPI (backend API)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/adesa46/HeartAttackDetection.git
   cd HeartAttackDetection
   ```

2. **Set up the Arduino**
   - Flash the Arduino firmware (see `test-demo/recieve.ino`)
   - Configure ECG lead connections
   - Verify Bluetooth module connectivity

3. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Initialize ML models**
   ```bash
   python models/cnn/test.py
   python models/lstm/test.py
   python models/rnn/test.py
   ```

## 📊 Signal Processing Pipeline

1. **Acquisition**: Raw ECG signals captured via 6-lead electrodes
2. **Conditioning**: Noise filtering and signal amplification (Arduino)
3. **Transmission**: Data sent via Bluetooth to mobile device
4. **Processing**: Signal normalization and feature extraction
5. **Analysis**: ML models evaluate cardiac patterns
6. **Interpretation**: Detection of anomalies or heart attack indicators
7. **Alert**: Notifications sent to user and emergency contacts

## 🔍 Testing & Demonstration

The `test-demo/` folder contains utilities for testing and validation:
- `signalprocess.py` - Signal processing algorithms
- `visualize.py` / `finervisualize.py` - ECG visualization tools
- `lstm_check.py` - Model validation
- `st_elevation_analysis.py` - ST segment analysis (critical for MI detection)
- `readtocsv.py` / `readtojson.py` - Data format conversion
- `ecg_denoised.csv` - Sample ECG dataset

## 📱 Mobile App Integration

### Live Tracking
- Real-time ECG waveform display
- Heart rate calculation and trend analysis
- Instant health alerts

### Recorded Tracking
- Access historical ECG recordings
- Detailed analysis reports
- Comparison with baseline data

### App Features
- **Emergency SOS**: Quick access to emergency contacts
- **Battery Status**: Device battery percentage and remaining recording time
- **Device Pairing**: Bluetooth connectivity management
- **System Diagnostics**: Electrode contact quality, signal strength
- **Health Insights**: AI-generated cardiac analysis summaries

## ⚠️ Safety & Medical Compliance

- **Disclaimer**: This device is intended for supplementary monitoring and should not replace professional medical diagnosis
- **Data Security**: All ECG data is encrypted and stored securely
- **Medical Review**: Consider validation with certified cardiologists
- **Emergency Protocols**: Ensure direct integration with emergency services

## 📈 Performance Metrics

- **Sampling Rate**: Real-time ECG acquisition capability
- **Detection Accuracy**: [To be filled after model training/validation]
- **Latency**: < 100ms detection to alert
- **Battery Life**: [To be filled based on device specifications]
- **Wireless Range**: ~10 meters (Bluetooth standard)

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Submit a pull request

## 📝 License

[Add your license information here]

## 📞 Contact & Support

For issues, questions, or contributions, please contact:
- **Primary Contact**: Ansh Desai ([adesa46@illinois.edu](mailto:adesa46@illinois.edu))
- **Repository**: [HeartAttackDetection](https://github.com/adesa46/HeartAttackDetection)
- **Contributors**: Ansh Desai, Aditya Kewalram, Srivarsh Gudlavalleti, Nandini Sharma

## 🔗 References

- ECG Signal Processing Standards
- Machine Learning for Healthcare
- Arduino Documentation
- Cardiac Event Detection Literature

---

**⚠️ Important Disclaimer**: This system is a research/prototype project. It should not be used as the sole basis for medical decisions. Always consult with healthcare professionals for cardiac conditions.
