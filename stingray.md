 
# Stingray Project Setup - Structured Notes  

## 1. **Clone the Project**  
- **If Git is installed:**  
  ```sh  
  git clone https://github.com/StingraySoftware/Stingray.git  
  cd Stingray  
  ```  
- **If Git is not installed:**  
  - Download the ZIP file manually  
  - Extract it  

---  

## 2. **Set Up Virtual Environment**  
- **Create Virtual Environment:**  
  ```sh  
  python -m venv venv  
  ```  
- **Change Execution Policy (Windows - Admin PowerShell):**  
  ```sh  
  Set-ExecutionPolicy Unrestricted -Scope CurrentUser  
  ```  
  - If prompted ("Do you want to change the execution policy?"), press **A** or **Y**.  

- **Activate Virtual Environment:**  
  - **Windows (CMD/PowerShell):**  
    ```sh  
    venv\Scripts\activate  
    ```  
  - **Mac/Linux:**  
    ```sh  
    source venv/bin/activate  
    ```  

---  

## 4. **Install Dependencies**  
- **If `requirements.txt` is available:**  
  ```sh  
  pip install -r requirements.txt  
  ```  
- **If the file is missing or an error occurs:**  
  ```sh  
  pip install numpy scipy matplotlib astropy  
  ```  
- If `requirements.txt` is inside the **docs folder**, run:  
  ```sh  
  pip install -r docs/requirements.txt  
  ```  
  - On Windows PowerShell, replace `/` with `\`:  
    ```sh  
    pip install -r docs\requirements.txt  
    ```  
  - Or first change to the **docs folder**:  
    ```sh  
    cd docs  
    pip install -r requirements.txt  
    ```  
---  

## 5. **Install the Project (Local Setup)**  
```sh  
pip install -e .  
```  
- This will install the project using `setup.py`.  

---  

## 6. **Select the Correct Python Interpreter in VS Code**  
- **If the virtual environment does not activate:**  
  1. **Open VS Code**  
  2. Press **CTRL + SHIFT + P**  
  3. **Search:**  
     ```
     Python: Select Interpreter  
     ```  
  4. **Select the Python interpreter for your virtual environment:**  
     ```
     C:\Users\mjawa\Pictures\git\Stingray\venv\Scripts\python.exe  
     ```  

---  

## 7. **Run the Code**  

### **Method 1: Python Interactive Shell**  
In Terminal:
```sh  
python  
```  
- Then run in the shell:  
  ```python  
  import stingray  
  print(stingray.__version__)  
  ```  
- **If an error occurs:**  
  ```sh  
  pip list | findstr stingray  
  ```  

### **Method 2: Test Script**  
- **Create a `test.py` file and write:**  
  ```python  
  from stingray import Lightcurve  
  import numpy as np  

  times = np.arange(0, 10, 0.1)  
  counts = np.random.poisson(100, len(times))  

  lc = Lightcurve(times, counts)  
  print(lc)  
  ```  
- **Run in the terminal:**  
  ```sh  
  python test.py  
  ```
  For this you should be in same path in which `test.py` exist.
  
- **If output appears, the setup is installed correctly.**  

---  

## 8. **Additional Resources**  
- **Stingray GitHub Repo:** [StingraySoftware/Stingray](https://github.com/StingraySoftware/Stingray)  
- **Documentation:** [Stingray Docs](https://stingray.readthedocs.io/)  
- **Issues & Discussions:** [GitHub Issues](https://github.com/StingraySoftware/Stingray/issues)  

- **If an error occurs:**  
  - Check logs  
  - Reinstall dependencies  
```
