FROM python:3.9
EXPOSE 8080

# Upgrade pip and install requirements
COPY requirements.txt .
RUN pip install -r requirements.txt

# Copy app code and set working directory
COPY . .

# Run
ENTRYPOINT ["streamlit", "run", "app.py", "--server.port=8080", "--server.address=0.0.0.0"]
CMD ["app.py", "--server.headless", "true", "--server.fileWatcherType", "none", "--browser.gatherUsageStats", "false"]