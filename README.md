~ Splunk Web Server Security Monitoring Project Notes ~

This project was designed and built to demonstrate my understanding of Splunk search language, dashboard building, and SIEM use cases.

Time Range Info

**To ensure the dashboard continues to work long after the log data was generated, 
all time ranges have been hardcoded in epoch format inside the dashboard XML.

{This dashboard is preconfigured to display sample data from:

**October 31 – November 1, 2025**}


This project simulates web server security monitoring using Splunk. It detects failed login attempts, suspicious user agents, brute force behavior, and common attack surface scans. It’s built on synthetic Apache logs to demonstrate detection and visualization in a real-world SIEM-like environment.

No setup required — just upload the web_access log file and open the dashboard.


List of Dash Panels and their Purpose:

1. Top Failed Login Attempts - Shows IP addresses with the highest number of failed login attempts (HTTP 401/403). Useful for detecting brute-force or credential stuffing attacks.
2. Geo Map of Suspicious IPs - Maps the geographic origin of failed login attempts using IP geolocation, helping identify suspicious regions or hotspots.
3. HTTP Status Codes Over Time - Visualizes trends in server response codes to detect spikes, errors, or scan behavior over time.
4. Top “Attack Tool” User Agents - Reveals the most common user agents behind failed login attempts. Helps identify automated tools like `sqlmap`, `curl`, or scripted scans.
5. Most-Requested Suspicious URIs - Lists the most frequently targeted endpoints such as `/admin`, `.env`, or `/phpmyadmin` — a strong signal of exploitation attempts.

📁 Files in This Repo

- web_access.log # Sample Apache access log with security noise
- dashboard.xml # Prebuilt Splunk dashboard 
- Dashboard Screenshots
- README.md # Project documentation
