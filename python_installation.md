## 1️⃣ Create the script file
```
vi install_python.sh
```
## 2️⃣ Paste this script
```
#!/bin/bash

echo "Updating system packages..."
sudo apt update
sudo apt upgrade -y

echo "Installing Python and required packages..."
sudo apt install -y python3 python3-pip python3-venv python3-dev build-essential

echo "Checking Python version..."
python3 --version

echo "Checking pip version..."
pip3 --version

echo "Creating a test virtual environment..."
python3 -m venv test_env

echo "Activating virtual environment..."
source test_env/bin/activate

echo "Python installed and virtual environment created successfully."

deactivate

```

## 3️⃣ Make the script executable
```
chmod +x install_python.sh
```

## 4️⃣ Run the script
```
./install_python.sh
```