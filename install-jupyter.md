# How to install jupyter

1. Install with pip a Python Package Manager

   ```bash
   pip install jupyter
   ```

2. Open Jupyter Notebook server port in firewall

    ```bash
    firewall-cmd --get-active-zones
    firewall-cmd --zone=public --add-port=8888/tcp
    ```