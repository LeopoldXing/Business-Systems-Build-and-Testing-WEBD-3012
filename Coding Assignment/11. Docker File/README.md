# Setup and Run Instructions

## Setup
1. Build the Docker image:

   ```shell
   docker build -t luping_xing_coding_assignment11 .
   ```

2. Run the Docker container:

   ```shell
   docker run -d -p 7775:7775 --name luping_xing_coding_assignment11 luping_xing_coding_assignment11
   ```



## Accessing the App

After starting the container, the React app will be available at `http://localhost:7775` on your browser. 