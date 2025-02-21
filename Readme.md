# PRIMARY ENERGY BY PRODUCTION/CONSUMPTION BY SOURCES
A publication of recent and historical U.S. energy statistics. This publication includes total energy production, consumption, stocks, and trade; energy prices; overviews of petroleum, natural gas, coal, electricity, nuclear energy, renewable energy, and carbon dioxide emissions; and data unit conversions values.
 
https://www.eia.gov/totalenergy/data/monthly/


## ENERGY ANALYSIS BY DATABASE

![The Energy Architecture](docs/primary_energy.drawio.png "The Energy Architecture")

---

## Step 1: Clone the GitHub Repository

### Explanation:
This step will download the code from the GitHub repository to your local machine. Cloning a repository means you're copying all the files, code, and resources from the remote repository to your local system.

```sh
git clone https://github.com/hanattaw/primary_energy.git
cd primary_energy
```

- `git clone https://github.com/hanattaw/primary_energy.git`: This command clones the `primary_energy` repository from GitHub to your local machine.
- `cd primary_energy`: This changes the current working directory to the `primary_energy` folder, which contains all the project files.

Now that the project is downloaded, you can work with the resources and configurations it provides.

---

## Step 2: Start Containers Using Docker Compose

### Explanation:
Docker Compose is used to define and run multi-container Docker applications. In this step, you're using Docker to start containers that will run PostgreSQL, MongoDB, and other services for your energy data analysis.

![Containers](docs/docker-compose.png "Container")

```sh
primary_energy $ docker compose up
```

- `docker compose up`: This command starts all the necessary containers defined in the `docker-compose.yml` file (such as PostgreSQL, MongoDB, and other services). It will pull the required Docker images and run them as containers. If it's your first time running it, Docker will download the images from the internet and start the containers.
- **Note:** You may need to have Docker installed on your machine before running this command. 

Once the containers are running, your PostgreSQL, MongoDB, and other services will be available locally.

---

## Step 3: Open PgAdmin (PostgreSQL Management)

### Explanation:
PgAdmin is a graphical user interface (GUI) for managing PostgreSQL databases. You’ll use it to interact with the `energy` database, view data, and run queries.

- Open your browser and navigate to: `http://localhost:5050`
- **Login Credentials:**
  - **Username:** `postgres`
  - **Password:** `postgres`
  - **Database:** `energy`

![PgAdmin](docs/pgadmin.png "PgAdmin")

### What you’ll do in PgAdmin:
- Once logged in, you can navigate to the `energy` database.
- You can view tables, run SQL queries, and manage the PostgreSQL database directly from PgAdmin.

---

## Step 4: Open MongoDB Compass (MongoDB Management)

### Explanation:
MongoDB Compass is a GUI tool that helps you interact with MongoDB databases. It provides a visual interface for querying and managing MongoDB collections.

- Open MongoDB Compass and connect using the following credentials:
  - **Connection string:** `mongodb://root:example@localhost:27017/`
  - **Username:** `root`
  - **Password:** `example`

![Compass](docs/mongodbcompass.png "Compass")

### What you’ll do in MongoDB Compass:
- After connecting, you can view the collections and documents stored in MongoDB.
- You can query and explore the data, making it easier to work with MongoDB and ensure that the energy data is stored correctly.

---

## Step 5: Open Grafana (Data Visualization)

### Explanation:
Grafana is a popular open-source platform for visualizing time-series data. In this setup, you will use Grafana to create interactive dashboards that display energy production, consumption, and other related data from your PostgreSQL and MongoDB databases.

- Open your browser and go to: `http://localhost:8085`
- **Login Credentials:**
  - **Username:** `admin`
  - **Password:** `admin`

![Grafana](docs/grafana.png "Grafana")

### What you’ll do in Grafana:
- Once logged in, you can start creating dashboards by adding data sources (PostgreSQL or MongoDB).
- Grafana supports time-series data, so you'll be able to create charts, graphs, and other visualizations based on energy data.
- You can also set up alerts to notify you of any important changes in the data.

---

## References
- [Total Energy Data from EIA](https://www.eia.gov/totalenergy/data/browser/index.php?tbl=T01.02#/?f=M): This link provides access to U.S. energy statistics, offering data related to energy production, consumption, and more, which you can use in the database for analysis and visualization.

---

### Summary of Each Step:

1. **Clone the GitHub repository** to get the necessary code and resources.
2. **Start Docker containers** using Docker Compose to set up PostgreSQL, MongoDB, and other services.
3. **Open PgAdmin** to manage the PostgreSQL database where energy data is stored.
4. **Open MongoDB Compass** to manage and view the MongoDB data used for energy analysis.
5. **Open Grafana** to visualize and create interactive dashboards for energy data analysis.

Each step sets up a different aspect of the energy data analysis environment, ensuring you have tools for managing data (PgAdmin, MongoDB Compass) and visualizing it (Grafana).

---
