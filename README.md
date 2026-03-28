# Smart Network Bandwidth Monitor

## Project Overview

Smart Network Bandwidth Monitor is a Python-based system monitoring tool that tracks internet usage in real-time and identifies which applications consume the most network bandwidth. This project helps users understand slow internet issues, monitor data usage, and detect unusual network activity.

The system continuously monitors upload and download speeds, analyzes network consumption, and visualizes the data using graphs for better understanding.

---

## Dataset

This project does not require any external dataset.
The data is generated dynamically from the system's real-time network usage.

The application collects:

* Upload speed
* Download speed
* Total data usage
* App-wise network consumption
* Time-based usage statistics

All data is gathered using system monitoring libraries.

---

## Language Used

This project is built using **Python** because:

* Python supports system-level monitoring
* Easy integration with networking libraries
* Strong visualization support
* Suitable for real-time applications

Python libraries used:

* **psutil** — for system and network monitoring
* **Streamlit** — for user interface
* **Matplotlib** — for data visualization
* **time** — for real-time tracking

---

## Installations

### Step 1: Install Python

Download Python from:
https://www.python.org/downloads/

---

### Step 2: Install Required Libraries

Open terminal and run:

```
pip install psutil streamlit matplotlib pandas
```

---

### Step 3: Run the Project

Navigate to project folder and run:

```
streamlit run network_monitor.py
```

---

## Project Structure

```
Smart-Network-Bandwidth-Monitor/
│
├── network_monitor.py
├── README.md
├── requirements.txt (optional)
```

---

## Structure of the Code

The project consists of the following sections:

### 1. Import Libraries

Libraries imported:

* psutil
* streamlit
* matplotlib
* pandas
* time

---

### 2. Network Monitoring Section

This section collects:

* Upload speed
* Download speed
* Total network usage

Using:

```
psutil.net_io_counters()
```

---

### 3. Real-Time Tracking

The system updates:

* Every few seconds
* Continuously monitors bandwidth
* Stores usage data

---

### 4. Data Visualization

Graphs generated:

* Download speed vs time
* Upload speed vs time
* Network usage comparison

---

### 5. Output Display

The application displays:

* Current upload speed
* Current download speed
* Bandwidth graphs
* Network usage summary

---

## Features

* Real-time bandwidth monitoring
* Upload and download tracking
* Graphical data visualization
* Lightweight and fast
* Easy-to-use interface

---

## Applications

* Students
* Developers
* Network administrators
* Personal system monitoring

---

## Future Enhancements

* App-wise network usage detection
* Data usage alerts
* Daily usage reports
* Bandwidth prediction

---

