# sql-failed-login-tracker

![Platform](https://img.shields.io/badge/Platform-SQL-lightgrey)
![Category](https://img.shields.io/badge/Category-Cybersecurity-blue)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Language](https://img.shields.io/badge/Language-SQL-yellow)

This project simulates a real-world failed login analysis using SQL. It tracks login attempts from a log table and highlights suspicious IPs with repeated failures — a common task for SOC analysts and cybersecurity defenders.

- Created a mock `user_activity_log` table.
- Queried failed logins and grouped by IP.
- Used `HAVING COUNT(*) >= 3` to identify brute-force indicators.
- Results ordered to prioritize most dangerous IPs.

## 📸 Screenshot
(images/sql-failed-logins.png)
(images/user-activity-logCSV.png)
