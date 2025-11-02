{\rtf1\ansi\ansicpg1252\cocoartf2761
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fnil\fcharset0 HelveticaNeue-Bold;\f1\fnil\fcharset0 HelveticaNeue;\f2\fnil\fcharset0 HelveticaNeue-Italic;
\f3\fnil\fcharset0 AppleColorEmoji;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc0\levelnfcn0\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{decimal\}.}{\leveltext\leveltemplateid1\'02\'00.;}{\levelnumbers\'01;}\fi-360\li720\lin720 }{\listname ;}\listid1}
{\list\listtemplateid2\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{hyphen\}}{\leveltext\leveltemplateid101\'01\uc0\u8259 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid2}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}{\listoverride\listid2\listoverridecount0\ls2}}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\deftab560
\pard\pardeftab560\partightenfactor0

\f0\b\fs40 \cf0 ~ Splunk Web Server Security Monitoring Project Notes ~\
\pard\pardeftab560\slleading20\pardirnatural\partightenfactor0

\f1\b0\fs26 \cf0 \
\pard\pardeftab560\slleading20\partightenfactor0

\f0\b \cf0 This project was designed and built to demonstrate my understanding of Splunk search language, dashboard building, and SIEM use cases.\
\pard\pardeftab560\slleading20\partightenfactor0

\f1\b0 \cf0 \
\pard\pardeftab560\slleading20\partightenfactor0

\f0\b \cf0 \ul \ulc0 Time Range Info
\f1\b0 \ulnone \
\
\pard\pardeftab560\slleading20\partightenfactor0

\f2\i \cf0 **To ensure the dashboard continues to work long after the log data was generated, \
all time ranges have been hardcoded in epoch format inside the dashboard XML.\
\
\{This dashboard is preconfigured to display sample data from:\
\
**October 31 \'96 November 1, 2025**\}
\f1\i0 \
\
\
This project simulates web server security monitoring using Splunk. It detects failed login attempts, suspicious user agents, brute force behavior, and common attack surface scans. It\'92s built on synthetic Apache logs to demonstrate detection and visualization in a real-world SIEM-like environment.\
\
No setup required \'97 just upload the web_access log file and open the dashboard.\
\
\
\pard\pardeftab560\slleading20\partightenfactor0

\f0\b \cf0 \ul List of Dash Panels and their Purpose:
\f1\b0 \ulnone \
\pard\pardeftab560\slleading20\pardirnatural\partightenfactor0
\cf0 \
\pard\pardeftab560\pardirnatural\partightenfactor0
\ls1\ilvl0\cf0 {\listtext	0.	}Top Failed Login Attempts - Shows IP addresses with the highest number of failed login attempts (HTTP 401/403). Useful for detecting brute-force or credential stuffing attacks.\
{\listtext	0.	}Geo Map of Suspicious IPs - Maps the geographic origin of failed login attempts using IP geolocation, helping identify suspicious regions or hotspots.\
{\listtext	0.	}HTTP Status Codes Over Time - Visualizes trends in server response codes to detect spikes, errors, or scan behavior over time.\
{\listtext	0.	}Top \'93Attack Tool\'94 User Agents - Reveals the most common user agents behind failed login attempts. Helps identify automated tools like `sqlmap`, `curl`, or scripted scans.\
{\listtext	0.	}Most-Requested Suspicious URIs - Lists the most frequently targeted endpoints such as `/admin`, `.env`, or `/phpmyadmin` \'97 a strong signal of exploitation attempts.\
\pard\pardeftab560\slleading20\partightenfactor0
\cf0 \

\f3 \uc0\u55357 \u56513 
\f2\i  Files in This Repo
\f1\i0 \
\
\pard\pardeftab560\pardirnatural\partightenfactor0
\ls2\ilvl0
\fs24 \cf0 {\listtext	\uc0\u8259 	}
\fs26 web_access.log # Sample Apache access log\
\ls2\ilvl0
\fs24 {\listtext	\uc0\u8259 	}
\fs26 dashboard.xml # Prebuilt Splunk dashboard \
\pard\pardeftab560\pardirnatural\partightenfactor0
\ls2\ilvl0\cf0 {\listtext	\uc0\u8259 	}README.md # Project documentation\
\pard\pardeftab560\pardirnatural\partightenfactor0
\ls2\ilvl0
\fs24 \cf0 {\listtext	\uc0\u8259 	}
\fs26 Dashboard Screenshots\
}
