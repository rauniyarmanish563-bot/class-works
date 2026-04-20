# 📊 NumPy & GitHub File Handling Project

## 📌 Description
This project demonstrates how to read a `.ipynb` file from a GitHub repository using Python in Google Colab and extract useful code from it.

## 🚀 Features
- Read file from GitHub using raw URL  
- Extract code from notebook  
- Use NumPy arrays  
- Run in Google Colab  

## 🛠️ Technologies Used
- Python  
- NumPy  
- Requests  
- JSON  

## 💻 Example Code
import requests
import json

url = "https://raw.githubusercontent.com/rauniyarmanisha563-bot/class-works/main/create%20an%20array%20by%20using%20numpy.ipynb"

response = requests.get(url)
data = json.loads(response.text)

for cell in data['cells']:
    if cell['cell_type'] == 'code':
        print("".join(cell['source']))

## ▶️ How to Run
1. Open Google Colab  
2. Paste the code  
3. Run it  

## 👨‍💻 Author
Manish Rauniyar
