# DarkScraper Advanced Reconnaissance System v6.0
# Requirements.txt Installation Guide

# 1. Optain DarkScraper through contacting AnonCatalyst or reaching NoTrac3 through their socials 

# 2. Recommended: Create a virtual environment
python3 -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate  # Windows

# 3. Install requirements with pip
pip install --upgrade pip
pip install --break-system-packages -r requirements.txt

# 4. Alternative: Install with pipx (isolated environment)
pipx install --spec git+https://github.com/NoTrac3/DarkScraper.git ars

### TROUBLESHOOTING ###

# If you get "externally-managed-environment" error:
# Use --break-system-packages flag (Python 3.11+)
pip install --break-system-packages -r requirements.txt

# If pipx fails:
# First install pipx properly
python3 -m pip install --user pipx
python3 -m pipx ensurepath
# Then install package
pipx install -r requirements.txt

# If selenium/geckodriver issues occur:
# Install Firefox and geckodriver
sudo apt install firefox -y
wget https://github.com/mozilla/geckodriver/releases/download/v0.34.0/geckodriver-v0.34.0-linux64.tar.gz
tar -xvzf geckodriver*
chmod +x geckodriver
sudo mv geckodriver /usr/local/bin/

# For permission errors:
python3 -m pip install --user --break-system-packages -r requirements.txt
