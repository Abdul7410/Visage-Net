

---

# Visage Net

**Visage Net** is a face recognition–powered system that automatically clusters and delivers personalized photos from large-scale events such as marathons, festivals, and weddings.  
It removes the manual effort of searching through thousands of images by accurately grouping photos by individual faces.

The project focuses on **face clustering, identity matching, and automated photo delivery**, enabling attendees to quickly reclaim their memories.

---

## Key Features

- Face detection and recognition from large image collections  
- Automatic face-based photo clustering  
- Supports thousands to millions of event images  
- Streamlit-based interactive web interface  
- YAML-based configuration management  
- Pickle-based storage for face encodings  
- High-accuracy matching using `face_recognition`  
- Scalable pipeline for event photo processing  


## Dependencies

```txt
streamlit
pyyaml
pickle-mixin
opencv-python==4.7.0.72
face_recognition==1.3.0
````

All required Python packages are listed in `requirements.txt`.

---

## Project Structure

```bash
Visage-Net/
│
├── assets/
│   └── UI images and static resources
│
├── database/
│   └── Stored face encodings and metadata
│
├── pages/
│   └── Streamlit multi-page application views
│
├── backend.py
│   └── Core face recognition and clustering logic
│
├── Upload_photos.py
│   └── Photo ingestion and preprocessing pipeline
│
├── utils.py
│   └── Shared utility functions and helpers
│
├── mailtemplate.html
│   └── Email template for photo delivery
│
├── config.yaml
│   └── Centralized configuration settings
│
├── requirements.txt
│   └── Python dependencies
│
├── README.md
│   └── Project documentation
```

---

## Folder & File Overview

### assets

Contains static resources used by the Streamlit interface.

### database

Stores serialized face encodings and identity mappings using pickle.

### pages

Streamlit pages used for navigation and feature separation.

### backend.py

Handles:

* Face encoding generation
* Face comparison and clustering
* Identity mapping logic

### Upload_photos.py

Responsible for:

* Bulk photo ingestion
* Image preprocessing
* Event image handling

### utils.py

Reusable helper functions including:

* Face encoding utilities
* File handling
* Configuration loading

### config.yaml

Central configuration file containing:

* Dataset paths
* Threshold values
* Application-level settings

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/Abdul7410/Visage-Net.git
cd Visage-Net
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Running the Application

Run the Streamlit app:

```bash
streamlit run backend.py
```

Or execute the photo ingestion pipeline:

```bash
python Upload_photos.py
```

---

## How It Works

1. Event photos are uploaded into the system.
2. Faces are detected and encoded using `face_recognition`.
3. Encodings are clustered based on facial similarity.
4. Photos are grouped per individual identity.
5. Personalized photo sets are prepared for delivery.
6. Attendees receive their photos automatically.

---

## Use Cases

* Marathon and sports event photo distribution
* Wedding and festival photo management
* Large-scale event photography workflows
* Face recognition and clustering research
* Computer vision and machine learning learning projects

---

## Future Enhancements

* Cloud-based photo storage integration
* Email and link-based photo delivery
* Improved clustering performance for large datasets
* User authentication and privacy controls

---

## License

This project is intended for educational and research purposes.

```
```







