import streamlit as st
import psutil
import pandas as pd
import time
from datetime import datetime

st.title("📡 Smart Network Bandwidth Monitor")

st.write("Real-time Upload and Download Speed")

# Create dataframe
data = pd.DataFrame(columns=["Time", "Upload", "Download"])

# Get initial values
old_value = psutil.net_io_counters()

# Button to start monitoring
if st.button("Start Monitoring"):

    for i in range(50):   # runs 50 times
        
        time.sleep(1)

        new_value = psutil.net_io_counters()

        upload = (new_value.bytes_sent - old_value.bytes_sent) / 1024
        download = (new_value.bytes_recv - old_value.bytes_recv) / 1024

        old_value = new_value

        current_time = datetime.now().strftime("%H:%M:%S")

        new_row = {
            "Time": current_time,
            "Upload": upload,
            "Download": download
        }

        data = pd.concat([data, pd.DataFrame([new_row])], ignore_index=True)

        st.write("Upload Speed:", round(upload,2), "KB/s")
        st.write("Download Speed:", round(download,2), "KB/s")

        st.line_chart(data.set_index("Time"))
