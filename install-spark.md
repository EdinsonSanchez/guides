# How to install Apache Spark

1. Download Spark tar file from https://spark.apache.org/downloads.html
2. Copy file to server

    ```bash
    scp spark-2.4.0-bin-hadoop2.7.tgz root@idesoft.co:~/
    ```

3. Extracting Spark tar file

    ```bash
    tar xvf spark-2.4.0-bin-hadoop2.7.tgz
    ```

4. Move Spark software files to respective directory

   ```bash
    mv spark-2.4.0-bin-hadoop2.7 /usr/local/spark
   ```

5. Configure the environment for Spark

   ```bash
   export PATH = $PATH:/usr/local/spark/bin
   ```

6. update bashrc

   ```bash
   source ~/.bashrc
   ```