# AdventureWorks Business Intelligence Dashboard

# Deutsch

## Geschäftliche Herausforderung

AdventureWorks ist ein weltweit tätiges Einzelhandels- und Fertigungsunternehmen, das Daten aus verschiedenen Geschäftsbereichen generiert – darunter Vertrieb, Kunden, Produkte, Vertriebsgebiete und Retouren.

Das Unternehmen steht vor mehreren Herausforderungen:

- Geschäftsdaten sind auf mehrere, nicht miteinander verknüpfte Quellen verteilt.
- Berichte werden manuell erstellt, was zu langsamen Entscheidungsprozessen führt.
- Vertriebsleitern fehlt der Echtzeit-Einblick in Umsatz, Gewinn und Produktperformance.
- Führungskräfte können Vertriebstrends, Kundenverhalten oder regionale Leistungen nicht ohne Weiteres erkennen.
- Es gibt kein zentrales Dashboard zur Überwachung der geschäftlichen Kennzahlen (KPIs).

Ziel ist es, ungefilterte Geschäftsdaten in eine skalierbare Business-Intelligence-Lösung zu überführen, die datengestützte Entscheidungen ermöglicht.

---

# Projektziel

Entwicklung einer vollständigen Power BI-Berichtslösung unter Einhaltung des gesamten BI-Workflows:

- Verbindung und Transformation von Rohdaten
- Aufbau eines optimierten relationalen Datenmodells
- Erstellung geschäftlicher Kennzahlen mittels DAX
- Design interaktiver Dashboards für Führungskräfte
- Veröffentlichung eines produktionsreifen Berichts

---

# Lösungsarchitektur

```
Rohdaten
│
▼
Power Query (ETL)
│
▼
Datenmodell (Sternschema)
│
▼
DAX-Geschäftslogik
│
▼
Interaktive Dashboards
│
▼
Power BI Service
```

---

# Projektablauf

## Phase 1 — Datenextraktion & -transformation (Power Query)

### Geschäftliche Herausforderung

Geschäftsinformationen stammen aus verschiedenen Quellen und weisen inkonsistente Formatierungen, Duplikate, fehlende Werte sowie überflüssige Spalten auf. Vor der Analyse müssen die Daten bereinigt und standardisiert werden.

### Lösung

Mithilfe von **Power Query** wurden die Daten durch einen automatisierten ETL-Prozess transformiert.

### Durchgeführte Aufgaben

- Verbindung zu mehreren Datenquellen hergestellt
- AdventureWorks-Datensätze importiert
- Rohdaten bereinigt und transformiert
- Duplikate entfernt
- Datentypen korrigiert
- Spalten aufgeteilt und zusammengeführt
- Bedingte Spalten erstellt
- Tabellen für rollierende Kalender erstellt
- Datensätze gruppiert und aggregiert
- Daten pivotiert und entpivotiert (Pivot/Unpivot)
- Abfragen zusammengeführt (Merge) und angehängt (Append)
- Wiederverwendbare Parameter erstellt
- Prüfungen der Datenqualität durchgeführt

### Ergebnis

Eine vollautomatisierte und wiederholbare Datenaufbereitungs-Pipeline, bereit für die Analyse.

---

## Phase 2 — Datenmodellierung

### Geschäftliche Herausforderung

Ohne ein geeignetes Datenmodell werden Berichte langsam, ungenau und schwer zu warten. ### Lösung

Entwurf eines skalierbaren relationalen Modells unter Einhaltung der Best Practices für Microsoft Power BI.

### Durchgeführte Aufgaben

- Erstellung von Fakten- und Dimensionstabellen
- Einrichtung von Beziehungen über Primär- und Fremdschlüssel
- Entwurf eines Sternschemas (Star Schema)
- Konfiguration der Beziehungskardinalität
- Verwaltung aktiver und inaktiver Beziehungen
- Steuerung der Filterrichtung
- Organisation des Modell-Layouts
- Hinzufügen von Hierarchien
- Konfiguration von Datenkategorien und -formaten

### Ergebnis

Ein optimiertes semantisches Modell, das schnelle Abfragen und präzises Reporting ermöglicht.

---

## Phase 3 – Geschäftsberechnungen (DAX)

### Geschäftliche Herausforderung

Rohdaten allein können wichtige geschäftliche Fragen nicht beantworten, wie zum Beispiel:

- Gesamtumsatz
- Gewinn
- Wachstumsrate
- Leistung im Vorjahr
- Laufende Summen (Running Totals)
- Customer Lifetime Value (Kundenlebenszeitwert)
- KPI-Vergleiche

### Lösung

Implementierung der Geschäftslogik mittels **Data Analysis Expressions (DAX).**

### Durchgeführte Aufgaben

- Erstellung berechneter Spalten
- Erstellung wiederverwendbarer Measures (Kennzahlen)
- Implementierung expliziter Measures
- Verwendung von Variablen zur Optimierung
- Anwendung von CALCULATE()
- Verwendung von FILTER()
- Anwendung von ALL()
- Erstellung von Iterator-Funktionen (SUMX, AVERAGEX usw.)
- Erstellung von Time-Intelligence-Berechnungen
- Implementierung von SWITCH()-Logik
- Verwendung von RELATED()
- Erstellung bedingter Kennzahlen

### Ergebnis

Dynamische geschäftliche Kennzahlen (KPIs), die unmittelbar auf Benutzerauswahlen reagieren.

## Phase 4 – Dashboard-Entwicklung

### Geschäftliche Herausforderung

Entscheidungsträger benötigen klare und interaktive Dashboards anstelle statischer Berichte.

### Lösung

Entwicklung von Dashboards für die Führungsebene unter Anwendung bewährter Methoden der Power-BI-Visualisierung.

### Dashboard-Funktionen

- KPI-Karten
- Dashboard zur Vertriebsleistung
- Kundenanalysen
- Produktleistung
- Geografische Vertriebsanalyse
- Interaktive Karten
- Trendanalyse
- Prognosen (Forecasting)
- Drill-Down
- Drill-Through
- Dynamische Slicer (Datenschnitte)
- Lesezeichen
- Navigationsschaltflächen
- Benutzerdefinierte Tooltips
- Bedingte Formatierung
- Top-N-Analyse
- Mobiles Layout
- Sicherheit auf Zeilenebene (RLS)
- Veröffentlichung im Power BI Service

### Ergebnis

Interaktive Dashboards, die es Nutzern ermöglichen, die Unternehmensleistung ohne technisches Fachwissen zu analysieren.

---

# Verwendete Technologien

| Tool | Zweck |
|------|---------|
| Power BI Desktop | Dashboard-Entwicklung |
| Power Query (M) | Datentransformation |
| DAX | Geschäftsberechnungen |
| DAX Studio | Leistungsanalyse |
| AdventureWorks-Datensatz | Beispiel-Geschäftsdaten | ---

# Wichtige Geschäftsergebnisse

Diese Lösung ermöglicht es den Beteiligten:

- Die unternehmensweite Vertriebsleistung zu überwachen
- Produkte mit der besten Performance zu identifizieren
- Das Kaufverhalten der Kunden zu analysieren
- Regionale Leistungen zu vergleichen
- KPIs in Echtzeit zu verfolgen
- Langfristige Verkaufstrends zu erkennen
- Die Entscheidungsfindung durch interaktive Dashboards zu verbessern
- Daten mittels Zeilenebene-Sicherheit (Row-Level Security) zu schützen
- Berichte über den Power BI Service zu teilen

---

# Angewandte Kompetenzen

### Datenaufbereitung

- ETL-Entwicklung
- Datenbereinigung
- Datentransformation
- Abfrageoptimierung
- Power Query (M)

### Datenmodellierung

- Sternschema (Star Schema)
- Modellierung von Fakten- und Dimensionstabellen
- Beziehungsmanagement
- Datennormalisierung
- Semantische Modellierung

### Datenanalyse

- DAX-Kennzahlen (Measures)
- Berechnete Spalten
- Zeitintelligenz (Time Intelligence)
- KPI-Entwicklung
- Geschäftskennzahlen

### Datenvisualisierung

- Dashboards für Führungskräfte (Executive Dashboards)
- Interaktive Berichte
- Drillthrough-Funktionalität
- Lesezeichen (Bookmarks)
- Dynamische Filterung
- Mobile Optimierung

---
# Endergebnis

Dieses Projekt demonstriert den vollständigen Business-Intelligence-Lebenszyklus mit Microsoft Power BI – von der Aufnahme und Transformation der Rohdaten bis hin zu fortgeschrittener Analyse und der Entwicklung von Dashboards für Führungskräfte.

---

# Repository Struktur

```
AdventureWorks-PowerBI/
│
├── Dataset/
│   ├── Customers.csv
│   ├── Products.csv
│   ├── Sales.csv
│   ├── Returns.csv
│   └── Calendar.csv
│
├── PowerBI/
│   └── AdventureWorks Dashboard.pbix
│
├── Images/
│   ├── Dashboard.png
│   ├── DataModel.png
│   └── ReportPages.png
│
└── README.md
```

---

# Kontakt

**Naki Saiyed**

**Business Intelligence & Data Analyst**

- 💼 LinkedIn: https://linkedin.com/in/saiyed-naki
- 💻 GitHub: https://github.com/saiyednaki

---

# English

## Business Problem

AdventureWorks is a global retail and manufacturing company that generates data from multiple business functions including sales, customers, products, territories, and returns.

The company faces several challenges:

- Business data is stored across multiple disconnected sources.
- Reports are created manually, resulting in slow decision-making.
- Sales managers lack real-time visibility into revenue, profit, and product performance.
- Executives cannot easily identify sales trends, customer behaviour, or regional performance.
- There is no centralised dashboard for monitoring business KPIs.

The objective is to transform raw business data into a scalable Business Intelligence solution that enables data-driven decision making.

---

# Project Objective

Develop a complete Power BI reporting solution by following the entire BI workflow:

- Connect and transform raw data
- Build an optimised relational data model
- Create business metrics using DAX
- Design interactive executive dashboards
- Publish a production-ready report

---

# Solution Architecture

```
Raw Data
    │
    ▼
Power Query (ETL)
    │
    ▼
Data Model (Star Schema)
    │
    ▼
DAX Business Logic
    │
    ▼
Interactive Dashboards
    │
    ▼
Power BI Service
```

---

# Project Workflow

## Stage 1 — Data Extraction & Transformation (Power Query)

### Business Challenge

Business information comes from multiple sources with inconsistent formatting, duplicate records, missing values, and unnecessary columns. Before analysis, the data must be cleaned and standardised.

### Solution

Using **Power Query**, the data was transformed through an automated ETL process.

### Tasks Performed

- Connected to multiple data sources
- Imported AdventureWorks datasets
- Cleaned and transformed raw data
- Removed duplicates
- Corrected data types
- Split and merged columns
- Created conditional columns
- Built rolling calendar tables
- Grouped and aggregated records
- Pivoted and unpivoted data
- Merged and appended queries
- Created reusable parameters
- Performed data quality checks

### Outcome

A fully automated and repeatable data preparation pipeline ready for analysis.

---

## Stage 2 — Data Modelling

### Business Challenge

Without a proper data model, reports become slow, inaccurate, and difficult to maintain.

### Solution

Designed a scalable relational model following Microsoft Power BI best practices.

### Tasks Performed

- Built Fact and Dimension tables
- Created Primary and Foreign Key relationships
- Designed a Star Schema
- Configured relationship cardinality
- Managed active and inactive relationships
- Controlled filter direction
- Organised model layout
- Added hierarchies
- Configured data categories and formats

### Outcome

An optimised semantic model that supports fast queries and accurate reporting.

---

## Stage 3 — Business Calculations (DAX)

### Business Challenge

Raw data alone cannot answer important business questions such as:

- Total Sales
- Profit
- Growth Rate
- Previous Year Performance
- Running Totals
- Customer Lifetime Value
- KPI comparisons

### Solution

Implemented business logic using **Data Analysis Expressions (DAX).**

### Tasks Performed

- Created calculated columns
- Built reusable measures
- Implemented explicit measures
- Used variables for optimisation
- Applied CALCULATE()
- Used FILTER()
- Applied ALL()
- Built iterator functions (SUMX, AVERAGEX, etc.)
- Created Time Intelligence calculations
- Implemented SWITCH() logic
- Used RELATED()
- Created conditional metrics

### Outcome

Dynamic business KPIs that respond instantly to user selections.

---

## Stage 4 — Dashboard Development

### Business Challenge

Decision-makers require clear and interactive dashboards instead of static reports.

### Solution

Designed executive-level dashboards using Power BI visualisation best practices.

### Dashboard Features

- KPI Cards
- Sales Performance Dashboard
- Customer Analytics
- Product Performance
- Geographic Sales Analysis
- Interactive Maps
- Trend Analysis
- Forecasting
- Drill Down
- Drill Through
- Dynamic Slicers
- Bookmarks
- Navigation Buttons
- Custom Tooltips
- Conditional Formatting
- Top N Analysis
- Mobile Layout
- Row-Level Security (RLS)
- Published to Power BI Service

### Outcome

Interactive dashboards enabling users to explore business performance without technical expertise.

---

# Technologies Used

| Tool | Purpose |
|------|---------|
| Power BI Desktop | Dashboard Development |
| Power Query (M) | Data Transformation |
| DAX | Business Calculations |
| DAX Studio | Performance Analysis |
| AdventureWorks Dataset | Sample Business Data |

---

# Key Business Outcomes

This solution enables stakeholders to:

- Monitor company-wide sales performance
- Identify top-performing products
- Analyse customer purchasing behavior
- Compare regional performance
- Track KPIs in real time
- Discover long-term sales trends
- Improve decision-making with interactive dashboards
- Secure data using Row-Level Security
- Share reports through Power BI Service

---

# Skills Demonstrated

### Data Preparation

- ETL Development
- Data Cleaning
- Data Transformation
- Query Optimisation
- Power Query (M)

### Data Modelling

- Star Schema
- Fact & Dimension Modeling
- Relationship Management
- Data Normalisation
- Semantic Modelling

### Data Analysis

- DAX Measures
- Calculated Columns
- Time Intelligence
- KPI Development
- Business Metrics

### Data Visualisation

- Executive Dashboards
- Interactive Reports
- Drillthrough
- Bookmarks
- Dynamic Filtering
- Mobile Optimisation

---

# Final Result

This project demonstrates the complete Business Intelligence lifecycle using Microsoft Power BI—from raw data ingestion and transformation to advanced analytics and executive dashboard development.

The final solution follows industry best practices in data preparation, modeling, DAX development, and visualization, resulting in a scalable, interactive, and production-ready reporting system.

# Repository Structure

```
AdventureWorks-PowerBI/
│
├── Dataset/
│   ├── Customers.csv
│   ├── Products.csv
│   ├── Sales.csv
│   ├── Returns.csv
│   └── Calendar.csv
│
├── PowerBI/
│   └── AdventureWorks Dashboard.pbix
│
├── Images/
│   ├── Dashboard.png
│   ├── DataModel.png
│   └── ReportPages.png
│
└── README.md
```

---

# Connect With Me

**Naki Saiyed**

**Business Intelligence & Data Analyst**

- 💼 LinkedIn: https://linkedin.com/in/saiyed-naki
- 💻 GitHub: https://github.com/saiyednaki
