# AI Text-to-SQL System

Translate natural language questions into SQL SELECT queries using AI models.

---

## Overview

This project implements a Natural Language to SQL (Text-to-SQL) system that
converts user questions into executable SQL queries.

The system is designed for **safe database querying** and only allows
**SELECT statements**, preventing any modification of database data.

---

## Features

- Natural language to SQL conversion
- Schema-aware SQL generation
- Query validation for safe execution
- SELECT-only query restriction
- PostgreSQL database support
- Modular architecture

---

## Example Query

Input:

Show employees who completed qualification in 2012

Generated SQL:

SELECT *  
FROM employee  
WHERE qualification_year = 2012;

---

## Project Structure

config/ – configuration files and database schema  
data/ – training dataset for fine-tuning  
src/ – core application modules  

Key modules:

- `sql_engine.py` → SQL generation and validation  
- `schema_loader.py` → schema parsing  
- `run_query.py` → query execution interface  
- `openai_finetune.py` → fine-tuning pipeline  

---

## Tech Stack

- Python
- OpenAI API
- PostgreSQL
- YAML configuration

---

## Safety

The system validates generated SQL queries and only allows:

SELECT statements

This prevents accidental updates, deletions, or schema changes.

---

## Future Improvements

- Streamlit web interface
- Query explanation
- Multi-database support
- Role-based query permissions
