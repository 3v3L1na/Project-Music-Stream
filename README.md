# 🎵 MusicStream Trends (2018‑2022)

> *Uncovering how global events reshaped our listening habits.*

---

## 📌 Project Overview

MusicStream Trends examines **Spotify** and **Last.fm** data between **2018‑2022** to answer questions like:

* How did the pandemic influence listening behaviour 📈?
* Which genres surged or faded 🎸🎹?
* What artists or tracks defined each year 👑?

The pipeline ⇒ **API ⇢ MySQL ⇢ Python ⇢ SQL + Visuals**.


---

## 🚀 Quick Start

```bash
# 1 . Install deps
pip install -r requirements.txt

# 2 . Extract data
python data_extraction.py

# 3 . Create schema & load tables
python database_setup.py
python data_loading.py

# 4 . Run sample query
mysql -u <user> -p < db.sql
```

---

## 📂 Project Structure

```
│  README.md
│  requirements.txt
├─data_extraction.py      # Spotify & Last.fm pullers
├─database_setup.py       # DDL (tables, indexes)
├─data_loading.py         # ETL into MySQL
├─notebooks/              # Exploratory & SQL notebooks
└─assets/                 # Slides, images, Genially links
```

---

## 🔑 Key Queries & Insights

```sql
-- Popular tracks during lockdown months (Mar‑Jun 2020)
SELECT title, artist, popularity
FROM   songs
WHERE  year = 2020 AND month BETWEEN 3 AND 6
ORDER BY popularity DESC
LIMIT 20;
```

---

## 🛠️ Tech Stack

| Layer      | Tools                                               |
| ---------- | --------------------------------------------------- |
| Extraction | `Python requests`, **Spotify API**, **Last.fm API** |
| Storage    | **MySQL Workbench 8**                               |
| Analysis   | `pandas`, `mysql‑connector‑python`                  |
| Visuals    | **Excel**, **Genially**                             |

---

## 👩‍💻 Team — **Insight Lab**

* **Evelina Saponjic**
* **Mai García**
* **Carla Vera**
* **Lorena Nuñez**
* **Susana García**
* **Elena Peña**

> Built with ☕, 🎧 & a lot of SQL love.

---

<p align="center"><em>Questions or suggestions? Open an issue or reach us via a pull request 🙌.</em></p>
