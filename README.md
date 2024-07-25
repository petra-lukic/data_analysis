# Trashevents Data Analysis

This repository contains code for analyzing food waste data captured by KITRO devices. The analysis includes metrics and visualizations to help understand food waste patterns and evaluate device performance. The data comes from various sources, including trashevent captures, outlets, properties, customers, and device deployments.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Setup Instructions](#setup-instructions)
3. [Usage](#usage)

## Project Overview

The project involves computing key metrics and creating visualizations to support business decisions related to food waste management. The data is extracted from a PostgreSQL database and analyzed using Python libraries.

**Key metrics include:**

- Average number of trashevents per device and per day.
- Customer with the most total weight of food waste measured and the total weight measured for this customer.
- The calendar month (over all years) with the most trashevents captured and the number of trashevents for this calendar month.

**Visualizations include:**

- Evolution of total weight measured per day.
- Number of active deployments per property.
- Daily average weight of food waste per device.

## Setup Instructions

### Prerequisites

- Python 3.11.5
- PostgreSQL Database access

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/petra-lukic/data_analysis.git
    cd data_analysis
    ```

2. **Create and activate a virtual environment (optional but recommended):**

    ```bash
    python -m venv venv
    ```

    - **On Windows:**

      ```bash
      venv\Scripts\activate
      ```

    - **On Mac or Linux:**

      ```bash
      source venv/bin/activate
      ```

3. **Install dependencies:**

    Use the `requirements.txt` file to install the necessary packages:

    ```bash
    pip install -r requirements.txt
    ```

4. **Set up environment variables:**

    - **On Windows:**

      ```bash
      echo DB_TYPE=postgresql > .env
      echo DB_DRIVER=psycopg2 >> .env
      echo DB_USERNAME=your_username >> .env
      echo DB_PASSWORD=your_password >> .env
      echo DB_HOST=your_host >> .env
      echo DB_PORT=your_port >> .env
      echo DB_NAME=your_database_name >> .env
      ```

    - **On Mac or Linux:**

      ```bash
      echo "DB_TYPE=postgresql" > .env
      echo "DB_DRIVER=psycopg2" >> .env
      echo "DB_USERNAME=your_username" >> .env
      echo "DB_PASSWORD=your_password" >> .env
      echo "DB_HOST=your_host" >> .env
      echo "DB_PORT=your_port" >> .env
      echo "DB_NAME=your_database_name" >> .env
      ```

    Replace `your_username`, `your_password`, `your_host`, `your_port` and `your_database_name` with your actual database connection information.

## Usage

Ensure your virtual environment is activated.

1. **Start Jupyter Notebook:**
    
    First install Jupyter Notebook:

    ```bash
    pip install notebook
    ```

    Then start Jupyter Notebook:

    ```bash
    jupyter notebook
    ```

2. **Open the Notebook:**

    In the Jupyter Notebook interface, navigate to the directory where you cloned the repository and open the `trashevents_data_analysis.ipynb` file.

3. **Run the Notebook:**

    Click on the "Run" menu at the top of the interface and select "Run All Cells" to execute all cells and view the analysis results.
