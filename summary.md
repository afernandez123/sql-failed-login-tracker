# SQL Failed Login Tracker 🔍

![Platform](https://img.shields.io/badge/Platform-SQL-lightgrey) 
![Category](https://img.shields.io/badge/Category-Threat_Detection-blue) 
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

# Analyst Report: SQL Failed Login Tracker 🔍

## 🧠 Executive Summary
This analysis identifies IP addresses with a high volume of failed login attempts, suggesting potential brute-force behavior. Data was extracted and analyzed using SQL logic on sample user activity logs.

## 📂 Dataset Overview
- **Source**: user_activity_log.csv
- **Fields**: timestamp, username, ip_address, action, success
- **Imported into**: security_logs.db (SQLite)

## 🧪 Detection Logic
sql
SELECT ip_address, COUNT(*) AS attempts
FROM user_activity
WHERE success = 'false'
GROUP BY ip_address
HAVING COUNT(*) >= 3
ORDER BY attempts DESC;
