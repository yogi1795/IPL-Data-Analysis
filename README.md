# 🏏 IPL Analytics Just Got Real – An End-to-End Microsoft Fabric Project
In this project, I challenged myself to turn **unstructured IPL match data** into a dynamic, interactive report—all using **Microsoft Fabric**. What began as a curiosity sparked by raw JSON files from CricSheet became an exercise in combining **data engineering, transformation, semantic modeling**, and **business intelligence**—all within one modern data platform.

### 🧠 Inspiration
It started with a simple stat:
**AB de Villiers** scored more IPL runs against **Jasprit Bumrah** and **Lasith Malinga** than against any other bowlers—two of the toughest death-over legends in T20 history.

That led me down a rabbit hole of cricket stats:

- **Chris Gayle** smashed 59 sixes in the 2012 season alone and holds the record for the highest individual IPL score: **175 not out**

- **Virat Kohli** scored a record-breaking 973 runs in the 2016 season, and has the highest number of IPL centuries: **8**

And I thought: what if I could make all this data explorable—by anyone—through a dynamic report using Fabric?

### 🛠️ Project Workflow
Here’s what I built—**end-to-end, using Microsoft Fabric**:

#### 📥 Step 1: Data Ingestion
- Downloaded the IPL JSON data directly from CricSheet using **PySpark** in a Fabric notebook

- Extracted and saved the data into a **Lakehouse** (Files section)

#### 🧹 Step 2: Data Transformation
- Used **PySpark notebooks** to parse and flatten the JSON

- Transformed innings-level and delivery-level stats into structured tabular data

- Stored the results into **Delta tables** within the Lakehouse

#### 🏗️ Step 3: Data Warehousing
- Built a **Warehouse** in Fabric

- Used a **pipeline with a ForEach activity** to:

- - Iterate through table names

- - Copy each dataset from Lakehouse into a **dedicated schema** in the Warehouse

- - Dynamically create new tables during the load

#### 📊 Step 4: Semantic Modeling and Reporting
- Created a **Semantic Model** on top of the cleaned Warehouse tables

- Connected the model to **Power BI**

- Built an interactive report exploring:

- - Top scorers by season

- - Most runs/sixes against specific bowlers

- - Player performance by team and venue

- - Trends in scoring across years

### 📈 Report Highlights
- Explore **century scorers, 50+ scores**, and **highest match performances**

- Drill into a player’s career across seasons

- See bowler vs batter head-to-head stats

- Filter by venue, year, team, or phase of innings

⚡ Want to know how many sixes Dhoni hit in the final overs?
Want to compare Kohli’s consistency vs Warner’s strike rate?
With DAX and Fabric, I made it possible.

### 🧠 Learnings and Reflections
- Fabric is extremely powerful for **end-to-end analytical workflows**

- You can **ingest, transform, model**, and **report** using only **Fabric-native services**

- I learned to handle **complex nested JSON**, dynamically manage schema creation, and build responsive dashboards using **Power BI**

