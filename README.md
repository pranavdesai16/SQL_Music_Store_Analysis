# 🎵 SQL Music Store Analysis using PostgreSQL

> A SQL portfolio project that analyzes a music store database using **PostgreSQL** to answer real-world business questions related to customers, sales, artists, genres, and revenue.

---

# 📌 Project Overview

This project explores the **Chinook Music Store Database** using **PostgreSQL**. The objective is to solve business-oriented analytical problems by writing SQL queries ranging from basic aggregations to advanced Common Table Expressions (CTEs) and Window Functions.

The project demonstrates practical SQL skills commonly used in Data Analyst and Business Intelligence roles.

---

# 🛠 Tech Stack

* **Database:** PostgreSQL
* **Language:** SQL
* **Tool:** pgAdmin (or PostgreSQL-compatible SQL Editor)
* **Version Control:** Git & GitHub

---

# 📂 Database Schema

The project uses the Chinook Music Store relational database.

<p align="center">
<img width="710" height="574" alt="MusicDatabaseSchema" src="https://github.com/user-attachments/assets/fd12f051-f2cb-49ef-8c2b-70ea62cdb52c" />

</p>

---

# 🗄 Database Tables

| Table         | Description              |
| ------------- | ------------------------ |
| Employee      | Employee information     |
| Customer      | Customer details         |
| Invoice       | Customer invoices        |
| InvoiceLine   | Purchased tracks         |
| Track         | Song information         |
| Album         | Album details            |
| Artist        | Artist information       |
| Genre         | Music genres             |
| Playlist      | Playlist information     |
| PlaylistTrack | Playlist-track mapping   |
| MediaType     | Audio format information |

---

# 🧠 SQL Concepts Used

* SELECT
* WHERE
* ORDER BY
* GROUP BY
* COUNT()
* SUM()
* AVG()
* INNER JOIN
* Subqueries
* Common Table Expressions (CTEs)
* Window Functions
* ROW_NUMBER()
* LIMIT

---

# 📈 Business Questions Solved

## 🟢 Easy Level

### 1. Who is the senior-most employee based on job title?

**Objective**

Find the employee with the highest job level.

**SQL Query**

> *(Insert screenshot below)*

<img width="652" height="142" alt="query_1" src="https://github.com/user-attachments/assets/8291acdb-708e-4b7c-aae3-06fcb91255a3" />

| Employee ID | Last Name | First Name | Title                  | Reports To | Level | Birthdate  | Hire Date  | Address            | City     | State | Country | Postal Code | Phone             | Fax               | Email                                                             |
| ----------: | --------- | ---------- | ---------------------- | ---------- | ----- | ---------- | ---------- | ------------------ | -------- | ----- | ------- | ----------- | ----------------- | ----------------- | ----------------------------------------------------------------- |
|           9 | Madan     | Mohan      | Senior General Manager | NULL       | L7    | 1961-01-26 | 2016-01-14 | 1008 Vrinda Ave MT | Edmonton | AB    | Canada  | T5K 2N1     | +1 (780) 428-9482 | +1 (780) 428-3457 | [madan.mohan@chinookcorp.com](mailto:madan.mohan@chinookcorp.com) |

---

### 2. Which countries have the most invoices?

**Objective**

Identify countries generating the highest number of invoices.

![Query 2](images/query2.png)
| Total Invoices | Billing Country |
| -------------: | --------------- |
|            131 | USA             |
|             76 | Canada          |
|             61 | Brazil          |
|             50 | France          |
|             41 | Germany         |
|             30 | Czech Republic  |
|             29 | Portugal        |
|             28 | United Kingdom  |
|             21 | India           |
|             13 | Chile           |
|             13 | Ireland         |
|             11 | Spain           |
|             11 | Finland         |
|             10 | Australia       |
|             10 | Netherlands     |
|             10 | Sweden          |
|             10 | Poland          |
|             10 | Hungary         |
|             10 | Denmark         |
|              9 | Austria         |
|              9 | Norway          |
|              9 | Italy           |
|              7 | Belgium         |
|              5 | Argentina       |

---

### 3. What are the top 3 invoice totals?

**Objective**

Retrieve the highest invoice amounts.

![Query 3](images/query3.png)
| Total |
| ----: |
| 23.76 |
| 19.80 |
| 19.80 |

---

### 4. Which city generated the highest revenue?

**Objective**

Determine the city with the highest total sales.

![Query 4](images/query4.png)
| Billing City        | Invoice Total |
| ------------------- | ------------: |
| Prague              |        273.24 |
| Mountain View       |        169.29 |
| London              |        166.32 |
| Berlin              |        158.40 |
| Paris               |        151.47 |
| São Paulo           |        129.69 |
| Dublin              |        114.84 |
| Delhi               |        111.87 |
| São José dos Campos |        108.90 |
| Brasília            |        106.92 |
| Lisbon              |        102.96 |
| Bordeaux            |         99.99 |
| Montréal            |         99.99 |
| Madrid              |         98.01 |
| Redmond             |         98.01 |
| Santiago            |         97.02 |
| Frankfurt           |         94.05 |
| Orlando             |         92.07 |
| Reno                |         91.08 |
| Ottawa              |         91.08 |
| Fort Worth          |         86.13 |
| Tucson              |         84.15 |
| Stuttgart           |         82.17 |
| Rio de Janeiro      |         82.17 |
| Porto               |         82.17 |
| Sidney              |         81.18 |
| New York            |         79.20 |
| Edinburgh           |         79.20 |
| Helsinki            |         79.20 |
| Budapest            |         78.21 |
| Madison             |         76.23 |
| Warsaw              |         76.23 |
| Yellowknife         |         75.24 |
| Stockholm           |         75.24 |
| Dijon               |         73.26 |
| Oslo                |         72.27 |
| Salt Lake City      |         72.27 |
| Chicago             |         71.28 |
| Bangalore           |         71.28 |
| Winnipeg            |         70.29 |
| Vienne              |         69.30 |
| Vancouver           |         66.33 |
| Boston              |         66.33 |
| Amsterdam           |         65.34 |
| Lyon                |         64.35 |
| Halifax             |         62.37 |
| Brussels            |         60.39 |
| Cupertino           |         54.45 |
| Rome                |         50.49 |
| Toronto             |         40.59 |
| Buenos Aires        |         39.60 |
| Copenhagen          |         37.62 |
| Edmonton            |         29.70 |

---

### 5. Who is the best customer?

**Objective**

Identify the customer who spent the most money.

![Query 5](images/query5.png)
| Customer ID | First Name | Last Name |  Total |
| ----------: | ---------- | --------- | -----: |
|           5 | R          | Madhav    | 144.54 |

---

# 🟡 Moderate Level

### 6. Rock Music Listeners

**Objective**

Retrieve customers who purchased Rock music.

![Query 6](images/query6.png)
| Email                                                                 | First Name | Last Name    |
| --------------------------------------------------------------------- | ---------- | ------------ |
| [aaronmitchell@yahoo.ca](mailto:aaronmitchell@yahoo.ca)               | Aaron      | Mitchell     |
| [alero@uol.com.br](mailto:alero@uol.com.br)                           | Alexandre  | Rocha        |
| [astrid.gruber@apple.at](mailto:astrid.gruber@apple.at)               | Astrid     | Gruber       |
| [bjorn.hansen@yahoo.no](mailto:bjorn.hansen@yahoo.no)                 | Bjørn      | Hansen       |
| [camille.bernard@yahoo.fr](mailto:camille.bernard@yahoo.fr)           | Camille    | Bernard      |
| [daan_peeters@apple.be](mailto:daan_peeters@apple.be)                 | Daan       | Peeters      |
| [diego.gutierrez@yahoo.ar](mailto:diego.gutierrez@yahoo.ar)           | Diego      | Gutiérrez    |
| [dmiller@comcast.com](mailto:dmiller@comcast.com)                     | Dan        | Miller       |
| [dominiquelefebvre@gmail.com](mailto:dominiquelefebvre@gmail.com)     | Dominique  | Lefebvre     |
| [edfrancis@yachoo.ca](mailto:edfrancis@yachoo.ca)                     | Edward     | Francis      |
| [eduardo@woodstock.com.br](mailto:eduardo@woodstock.com.br)           | Eduardo    | Martins      |
| [ellie.sullivan@shaw.ca](mailto:ellie.sullivan@shaw.ca)               | Ellie      | Sullivan     |
| [emma_jones@hotmail.com](mailto:emma_jones@hotmail.com)               | Emma       | Jones        |
| [enrique_munoz@yahoo.es](mailto:enrique_munoz@yahoo.es)               | Enrique    | Muñoz        |
| [fernadaramos4@uol.com.br](mailto:fernadaramos4@uol.com.br)           | Fernanda   | Ramos        |
| [fharris@google.com](mailto:fharris@google.com)                       | Frank      | Harris       |
| [fralston@gmail.com](mailto:fralston@gmail.com)                       | Frank      | Ralston      |
| [ftremblay@gmail.com](mailto:ftremblay@gmail.com)                     | François   | Tremblay     |
| [fzimmermann@yahoo.de](mailto:fzimmermann@yahoo.de)                   | Fynn       | Zimmermann   |
| [hannah.schneider@yahoo.de](mailto:hannah.schneider@yahoo.de)         | Hannah     | Schneider    |
| [hholy@gmail.com](mailto:hholy@gmail.com)                             | Helena     | Holý         |
| [hleacock@gmail.com](mailto:hleacock@gmail.com)                       | Heather    | Leacock      |
| [hughoreilly@apple.ie](mailto:hughoreilly@apple.ie)                   | Hugh       | O'Reilly     |
| [isabelle_mercier@apple.fr](mailto:isabelle_mercier@apple.fr)         | Isabelle   | Mercier      |
| [jacksmith@microsoft.com](mailto:jacksmith@microsoft.com)             | Jack       | Smith        |
| [jenniferp@rogers.ca](mailto:jenniferp@rogers.ca)                     | Jennifer   | Peterson     |
| [jfernandes@yahoo.pt](mailto:jfernandes@yahoo.pt)                     | João       | Fernandes    |
| [joakim.johansson@yahoo.se](mailto:joakim.johansson@yahoo.se)         | Joakim     | Johansson    |
| [johavanderberg@yahoo.nl](mailto:johavanderberg@yahoo.nl)             | Johannes   | Van der Berg |
| [johngordon22@yahoo.com](mailto:johngordon22@yahoo.com)               | John       | Gordon       |
| [jubarnett@gmail.com](mailto:jubarnett@gmail.com)                     | Julia      | Barnett      |
| [kachase@hotmail.com](mailto:kachase@hotmail.com)                     | Kathy      | Chase        |
| [kara.nielsen@jubii.dk](mailto:kara.nielsen@jubii.dk)                 | Kara       | Nielsen      |
| [ladislav_kovacs@apple.hu](mailto:ladislav_kovacs@apple.hu)           | Ladislav   | Kovács       |
| [leonekohler@surfeu.de](mailto:leonekohler@surfeu.de)                 | Leonie     | Köhler       |
| [lucas.mancini@yahoo.it](mailto:lucas.mancini@yahoo.it)               | Lucas      | Mancini      |
| [luisg@embraer.com.br](mailto:luisg@embraer.com.br)                   | Luís       | Gonçalves    |
| [luisrojas@yahoo.cl](mailto:luisrojas@yahoo.cl)                       | Luis       | Rojas        |
| [manoj.pareek@rediff.com](mailto:manoj.pareek@rediff.com)             | Manoj      | Pareek       |
| [marc.dubois@hotmail.com](mailto:marc.dubois@hotmail.com)             | Marc       | Dubois       |
| [mark.taylor@yahoo.au](mailto:mark.taylor@yahoo.au)                   | Mark       | Taylor       |
| [marthasilk@gmail.com](mailto:marthasilk@gmail.com)                   | Martha     | Silk         |
| [masampaio@sapo.pt](mailto:masampaio@sapo.pt)                         | Madalena   | Sampaio      |
| [michelleb@aol.com](mailto:michelleb@aol.com)                         | Michelle   | Brooks       |
| [mphilips12@shaw.ca](mailto:mphilips12@shaw.ca)                       | Mark       | Philips      |
| [nschroder@surfeu.de](mailto:nschroder@surfeu.de)                     | Niklas     | Schröder     |
| [patrick.gray@aol.com](mailto:patrick.gray@aol.com)                   | Patrick    | Gray         |
| [phil.hughes@gmail.com](mailto:phil.hughes@gmail.com)                 | Phil       | Hughes       |
| [puja_srivastava@yahoo.in](mailto:puja_srivastava@yahoo.in)           | Puja       | Srivastava   |
| [r.madhav@jetbrains.com](mailto:r.madhav@jetbrains.com)               | R          | Madhav       |
| [ricunningham@hotmail.com](mailto:ricunningham@hotmail.com)           | Richard    | Cunningham   |
| [robbrown@shaw.ca](mailto:robbrown@shaw.ca)                           | Robert     | Brown        |
| [roberto.almeida@riotur.gov.br](mailto:roberto.almeida@riotur.gov.br) | Roberto    | Almeida      |
| stanisław.wó[jcik@wp.pl](mailto:jcik@wp.pl)                           | Stanisław  | Wójcik       |
| [steve.murray@yahoo.uk](mailto:steve.murray@yahoo.uk)                 | Steve      | Murray       |
| [terhi.hamalainen@apple.fi](mailto:terhi.hamalainen@apple.fi)         | Terhi      | Hämäläinen   |
| [tgoyer@apple.com](mailto:tgoyer@apple.com)                           | Tim        | Goyer        |
| [vstevens@yahoo.com](mailto:vstevens@yahoo.com)                       | Victor     | Stevens      |
| [wyatt.girard@yahoo.fr](mailto:wyatt.girard@yahoo.fr)                 | Wyatt      | Girard       |

---

### 7. Top 10 Rock Artists

**Objective**

Find artists with the highest number of Rock tracks.

![Query 7](images/query7.png)
| Artist ID | Artist Name                  | Number of Songs |
| --------: | ---------------------------- | --------------: |
|        22 | Led Zeppelin                 |             114 |
|       150 | U2                           |             112 |
|        58 | Deep Purple                  |              92 |
|        90 | Iron Maiden                  |              81 |
|       118 | Pearl Jam                    |              54 |
|       152 | Van Halen                    |              52 |
|        51 | Queen                        |              45 |
|       142 | The Rolling Stones           |              41 |
|        76 | Creedence Clearwater Revival |              40 |
|        52 | Kiss                         |              35 |

---

### 8. Tracks Longer Than Average

**Objective**

List songs longer than the average track duration.

![Query 8](images/query8.png)
| Track Name                        | Duration (Milliseconds) |
| --------------------------------- | ----------------------: |
| Occupation / Precipice            |               5,286,953 |
| Through a Looking Glass           |               5,088,838 |
| Greetings from Earth, Pt. 1       |               2,960,293 |
| The Man With Nine Lives           |               2,956,998 |
| Battlestar Galactica, Pt. 2       |               2,956,081 |
| Battlestar Galactica, Pt. 1       |               2,952,702 |
| Murder On the Rising Star         |               2,935,894 |
| Battlestar Galactica, Pt. 3       |               2,927,802 |
| Take the Celestra                 |               2,927,677 |
| Fire In Space                     |               2,926,593 |
| The Long Patrol                   |               2,925,008 |
| The Magnificent Warriors          |               2,924,716 |
| The Living Legend, Pt. 1          |               2,924,507 |
| The Gun On Ice Planet Zero, Pt. 2 |               2,924,341 |
| The Hand of God                   |               2,924,007 |
| Experiment In Terra               |               2,923,548 |
| War of the Gods, Pt. 2            |               2,923,381 |
| The Living Legend, Pt. 2          |               2,923,298 |
| War of the Gods, Pt. 1            |               2,922,630 |
| Lost Planet of the Gods, Pt. 1    |               2,922,547 |
| Baltar's Escape                   |               2,922,088 |
| The Lost Warrior                  |               2,920,045 |
| Lost Planet of the Gods, Pt. 2    |               2,914,664 |
| The Gun On Ice Planet Zero, Pt. 1 |               2,907,615 |
| Greetings from Earth, Pt. 2       |               2,903,778 |
| Crossroads, Pt. 2                 |               2,869,953 |

---

# 🔴 Advanced Level

### 9. Customer Spending by Artist

**Objective**

Calculate how much each customer spent on the best-selling artist.

![Query 9](images/query9.png)
## Query 9: Amount Spent by Each Customer on Queen

```sql
-- Your SQL query here
```

**Output**

| Customer ID | First Name | Last Name    | Artist | Amount Spent |
| ----------: | ---------- | ------------ | ------ | -----------: |
|          46 | Hugh       | O'Reilly     | Queen  |        27.72 |
|          38 | Niklas     | Schröder     | Queen  |        18.81 |
|           3 | François   | Tremblay     | Queen  |        17.82 |
|          34 | João       | Fernandes    | Queen  |        16.83 |
|          53 | Phil       | Hughes       | Queen  |        11.88 |
|          41 | Marc       | Dubois       | Queen  |        11.88 |
|          47 | Lucas      | Mancini      | Queen  |        10.89 |
|          33 | Ellie      | Sullivan     | Queen  |        10.89 |
|          20 | Dan        | Miller       | Queen  |         3.96 |
|           5 | R          | Madhav       | Queen  |         3.96 |
|          23 | John       | Gordon       | Queen  |         2.97 |
|          54 | Steve      | Murray       | Queen  |         2.97 |
|          31 | Martha     | Silk         | Queen  |         2.97 |
|          16 | Frank      | Harris       | Queen  |         1.98 |
|          17 | Jack       | Smith        | Queen  |         1.98 |
|          24 | Frank      | Ralston      | Queen  |         1.98 |
|          30 | Edward     | Francis      | Queen  |         1.98 |
|          35 | Madalena   | Sampaio      | Queen  |         1.98 |
|          36 | Hannah     | Schneider    | Queen  |         1.98 |
|          11 | Alexandre  | Rocha        | Queen  |         1.98 |
|           8 | Daan       | Peeters      | Queen  |         1.98 |
|          42 | Wyatt      | Girard       | Queen  |         1.98 |
|          44 | Terhi      | Hämäläinen   | Queen  |         1.98 |
|           1 | Luís       | Gonçalves    | Queen  |         1.98 |
|          48 | Johannes   | Van der Berg | Queen  |         1.98 |
|          49 | Stanisław  | Wójcik       | Queen  |         1.98 |
|          52 | Emma       | Jones        | Queen  |         1.98 |
|          57 | Luis       | Rojas        | Queen  |         1.98 |
|          15 | Jennifer   | Peterson     | Queen  |         1.98 |
|          28 | Julia      | Barnett      | Queen  |         1.98 |
|          27 | Patrick    | Gray         | Queen  |         0.99 |
|          58 | Manoj      | Pareek       | Queen  |         0.99 |
|          45 | Ladislav   | Kovács       | Queen  |         0.99 |
|          26 | Richard    | Cunningham   | Queen  |         0.99 |
|          59 | Puja       | Srivastava   | Queen  |         0.99 |
|          13 | Fernanda   | Ramos        | Queen  |         0.99 |
|           6 | Helena     | Holý         | Queen  |         0.99 |
|          22 | Heather    | Leacock      | Queen  |         0.99 |
|          19 | Tim        | Goyer        | Queen  |         0.99 |
|          39 | Camille    | Bernard      | Queen  |         0.99 |
|          55 | Mark       | Taylor       | Queen  |         0.99 |
|          50 | Enrique    | Muñoz        | Queen  |         0.99 |
|          43 | Isabelle   | Mercier      | Queen  |         0.99 |

---

### 10. Most Popular Genre by Country

**Objective**

Identify the most purchased music genre in every country.

![Query 10](images/query10.png)
| Purchases | Country        | Genre              | Genre ID |
| --------: | -------------- | ------------------ | -------: |
|        17 | Argentina      | Alternative & Punk |        4 |
|        34 | Australia      | Rock               |        1 |
|        40 | Austria        | Rock               |        1 |
|        26 | Belgium        | Rock               |        1 |
|       205 | Brazil         | Rock               |        1 |
|       333 | Canada         | Rock               |        1 |
|        61 | Chile          | Rock               |        1 |
|       143 | Czech Republic | Rock               |        1 |
|        24 | Denmark        | Rock               |        1 |
|        46 | Finland        | Rock               |        1 |
|       211 | France         | Rock               |        1 |
|       194 | Germany        | Rock               |        1 |
|        44 | Hungary        | Rock               |        1 |
|       102 | India          | Rock               |        1 |
|        72 | Ireland        | Rock               |        1 |
|        35 | Italy          | Rock               |        1 |
|        33 | Netherlands    | Rock               |        1 |
|        40 | Norway         | Rock               |        1 |
|        40 | Poland         | Rock               |        1 |
|       108 | Portugal       | Rock               |        1 |
|        46 | Spain          | Rock               |        1 |
|        60 | Sweden         | Rock               |        1 |
|       166 | United Kingdom | Rock               |        1 |
|       561 | USA            | Rock               |        1 |

---

### 11. Top Customer by Country

**Objective**

Determine the highest spending customer in each country.

![Query 11](images/query11.png)
| Customer ID | First Name | Last Name    | Billing Country | Total Spending |
| ----------: | ---------- | ------------ | --------------- | -------------: |
|          56 | Diego      | Gutiérrez    | Argentina       |          39.60 |
|          55 | Mark       | Taylor       | Australia       |          81.18 |
|           7 | Astrid     | Gruber       | Austria         |          69.30 |
|           8 | Daan       | Peeters      | Belgium         |          60.39 |
|           1 | Luís       | Gonçalves    | Brazil          |         108.90 |
|           3 | François   | Tremblay     | Canada          |          99.99 |
|          57 | Luis       | Rojas        | Chile           |          97.02 |
|           5 | R          | Madhav       | Czech Republic  |         144.54 |
|           9 | Kara       | Nielsen      | Denmark         |          37.62 |
|          44 | Terhi      | Hämäläinen   | Finland         |          79.20 |
|          42 | Wyatt      | Girard       | France          |          99.99 |
|          37 | Fynn       | Zimmermann   | Germany         |          94.05 |
|          45 | Ladislav   | Kovács       | Hungary         |          78.21 |
|          58 | Manoj      | Pareek       | India           |         111.87 |
|          46 | Hugh       | O'Reilly     | Ireland         |         114.84 |
|          47 | Lucas      | Mancini      | Italy           |          50.49 |
|          48 | Johannes   | Van der Berg | Netherlands     |          65.34 |
|           4 | Bjørn      | Hansen       | Norway          |          72.27 |
|          49 | Stanisław  | Wójcik       | Poland          |          76.23 |
|          34 | João       | Fernandes    | Portugal        |         102.96 |
|          50 | Enrique    | Muñoz        | Spain           |          98.01 |
|          51 | Joakim     | Johansson    | Sweden          |          75.24 |
|          53 | Phil       | Hughes       | United Kingdom  |          98.01 |
|          17 | Jack       | Smith        | USA             |          98.01 |

---

# 💡 Key Learning Outcomes

Through this project, I gained practical experience in:

* Writing complex SQL queries
* Working with relational databases
* Performing multi-table joins
* Using aggregate functions
* Implementing subqueries
* Building Common Table Expressions (CTEs)
* Applying Window Functions
* Solving business-oriented SQL problems
* Analyzing customer purchasing behavior
* Generating actionable business insights

---

# 📁 Project Structure

```text
SQL-Music-Store-Analysis/
│
├── README.md
├── Music_Store_Analysis.sql
├── Dataset/
│
├── images/
│   ├── database_schema.png
│   ├── query1.png
│   ├── query2.png
│   ├── query3.png
│   ├── query4.png
│   ├── query5.png
│   ├── query6.png
│   ├── query7.png
│   ├── query8.png
│   ├── query9.png
│   ├── query10.png
│   └── query11.png
│
└── presentation/
    └── SQL_Music_Store_Analysis.pptx
```

---

# 🚀 Future Improvements

* Add interactive Power BI dashboard
* Build Tableau visualizations
* Write additional business-focused SQL queries
* Optimize query performance
* Perform exploratory data analysis using Python

---

# 📬 Connect With Me

**GitHub:** https://github.com/yourusername

**LinkedIn:** https://linkedin.com/in/yourprofile

**Email:** [your.email@example.com](mailto:your.email@example.com)

---

⭐ If you found this project useful, consider giving the repository a **Star**.
