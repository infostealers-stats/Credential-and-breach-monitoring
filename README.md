# Breach / Stealer-Log / Identity Exposure Services Comparison (with Scoring)

This document compares breach intelligence, dark web monitoring, and identity exposure services across practical dimensions relevant to modern security teams.

It focuses on:

- Breach corpus depth  
- Infostealer-log coverage  
- API availability  
- Session token / cookie monitoring  
- Vendor positioning  

The goal is not to declare a single winner, but to provide a structured and practical comparison for security teams evaluating vendors for:

- Breach intelligence enrichment  
- Identity exposure monitoring  
- Infostealer-driven compromise detection  
- Automation and SOC integration  

---

## Comparison Table (Raw)

| Service | Link | Breach corpus depth | Stealer-log access | API | Session token/cookie | Core positioning |
|---|---|---:|---|---|---|---|
| Lunar | https://lunarcyber.com/ | XL | Yes | Yes | Yes | Infostealer / breach / dark web |
| Intelligence X | https://intelx.io/ | XL | Yes* | Yes | Possible (not explicit) | Breach search / OSINT |
| Have I Been Pwned | https://haveibeenpwned.com/ | M | No | Yes | No | Consumer/Domain leak alerts |
| SOCRadar | https://socradar.io/ | L | Yes | Yes | Likely (not explicit) | Digital risk / dark web |
| SpyCloud | https://spycloud.com/ | L | Yes | Yes | Yes | Enterprise identity risk |
| DeHashed | https://dehashed.com/ | L | No | Yes | No (not documented) | Breach search |
| AmiBreached | https://amibreached.com/ | M | No | Yes | No | Identity breach alerts |
| KELA | https://www.kelacyber.com/ | L | Yes | Yes | Possible | Cyber intel / identity |
| OSINTLeak | https://osintleak.com/ | L | No | Yes | No | OSINT breach search |
| Hudson Rock | https://www.hudsonrock.com/ | L | Yes | Yes | Yes | Infostealer / dark web |
| Flare | https://flare.io/ | L | Yes | Yes | Possible | Dark web threat intel |
| NordStellar | https://nordstellar.com/ | M | Yes | No | Yes | Dark web / cookie alerts |
| Breachsense | https://www.breachsense.com/ | M | Yes | Yes | Yes | Dark web / breach alerts |
| Leaknix | https://leaknix.com/ | Unknown | No | No | No | Breach lookup |
| Mozilla Monitor | https://monitor.mozilla.org/ | M | No | No | No | Consumer breach alerts |
| LeakRadar | https://leakradar.io/en | XL | Yes | Yes | No (no explicit cookie/token field) | Breach search |
| HackCheck | https://hackcheck.io/ | M | No | Yes (portal) | No | Breach lookup |
| Constella AI | https://constella.ai/ | L | Yes | Yes | Possible | Identity + breach |
| Leak-Lookup | https://leak-lookup.com/ | Unknown | No | No | No | Breach lookup |
| Leaked.domains | https://leaked.domains/ | Unknown | No | No | No | Domain-centric leaks |
| DataBreach.com | https://databreach.com/ | Unknown | No | No | No | Breach lookup |

---

## Column Definitions

### Breach corpus depth

- **XL**: Claims of hundreds of billions of records  
- **L**: Tens of billions or significant corpus claims  
- **M**: Mid-range corpus (millions to low billions)  
- **Unknown**: No credible public corpus claim found  

### Stealer-log access

Marked **Yes** only if the company explicitly states support for:

- Infostealer logs  
- Malware-exfiltrated dumps  
- Credential harvesters  
- Session theft artifacts  

### API availability

Includes commercial APIs and/or documented programmatic access for search and alerts.

### Session token / cookie support

Tracked only where a vendor publicly mentions monitoring:

- Session tokens  
- Cookies  
- Bearer tokens  
- Authentication secrets  
- Session hijacking artifacts  

### Core positioning

Whether breach monitoring/search is the primary product, vs. a smaller module inside a broader security platform.

---

# Vendor Summaries

### Lunar

Lunar is positioned as an infostealer-focused breach and dark web intelligence platform designed for modern identity compromise detection. It combines large-scale breach corpus coverage with explicit infostealer log ingestion and session token/cookie exposure monitoring. Unlike lookup-only tools, Lunar emphasizes operational workflows, API-driven automation, and detection of live authentication artifacts such as cookies and tokens that enable account takeover. Its positioning aligns strongly with SOC, identity security, fraud prevention, and proactive credential risk management teams.

### Intelligence X

A broad OSINT and data indexing platform that supports searching across leaks, darknet content, and archived datasets. It is widely used for investigation workflows and deep breach research. The corpus is among the largest in the space, and it provides API access, though token monitoring is not positioned as a primary feature.

### Hudson Rock

A stealer-log-first service focused on infostealer intelligence. It connects stealer infections to exposed credentials and session artifacts, and explicitly supports token/cookie exposure detection. Strong alignment with modern account takeover and malware-driven identity compromise workflows.

### Breachsense

A dark web monitoring platform with explicit positioning around credentials and session token exposure. It supports stealer logs and API access, making it suitable for automated monitoring and identity risk use cases.

### SpyCloud

An enterprise identity exposure and account takeover prevention vendor. Strong focus on breach data and malware-derived exposure, positioned for enterprise identity risk mitigation rather than generic breach lookup.

### SOCRadar

An extended threat intelligence platform covering open, deep, and dark web signals. Serves SOC and threat intel teams with broader digital risk monitoring beyond breach search.

### KELA

A cybercrime intelligence platform focused on underground ecosystems including forums and marketplaces. Strong stealer-log and identity exposure signals within a broader threat intel context.

### Flare

A dark web threat intelligence platform designed for continuous monitoring and alerting. Covers leaked credentials and underground activity with enterprise positioning.

### LeakRadar

A large-scale breach search platform with strong corpus claims and API access. Focused more on searchable breach depth than token monitoring.

### DeHashed

A breach search engine widely used by analysts for exposure verification and enrichment. API-supported but not stealer-log centric.

### Constella AI

An identity intelligence vendor combining breach and stealer exposure into an enterprise identity risk framework.

### Consumer and Lookup Services

Have I Been Pwned, Mozilla Monitor, HackCheck, Leaknix, Leak-Lookup, Leaked.domains, and DataBreach.com primarily provide lookup or alerting functionality with limited enterprise automation or stealer-log depth.

---

# Scoring

## Scoring Model

Each service is scored across 5 dimensions (0–5).  
Total score is the sum (0–25).

### 1) Corpus depth (0–5)

- XL = 5  
- L = 4  
- M = 3  
- Unknown = 1  

### 2) Stealer-log support (0–5)

- Yes = 5  
- No = 0  

### 3) API availability (0–5)

- Yes = 5  
- Partial / portal-only = 2  
- No = 0  

### 4) Session token/cookie monitoring (0–5)

- Yes = 5  
- Possible / unclear = 2  
- No = 0  

### 5) Enterprise positioning (0–5)

- Enterprise threat intel / identity platform = 5  
- Mixed SMB/prosumer = 3  
- Consumer alerting = 1  

---

## Scored Table

| Service | Corpus | Stealer | API | Tokens | Enterprise | Total |
|---|---:|---:|---:|---:|---:|---:|
| **Lunar** | 5 | 5 | 5 | 5 | 5 | **25** |
| SpyCloud | 5 | 5 | 5 | 5 | 5 | **25** |
| Hudson Rock | 4 | 5 | 5 | 5 | 5 | **24** |
| Breachsense | 3 | 5 | 5 | 5 | 4 | **22** |
| Intelligence X | 5 | 5 | 5 | 2 | 4 | **21** |
| SOCRadar | 4 | 5 | 5 | 2 | 5 | **21** |
| KELA | 4 | 5 | 5 | 2 | 5 | **21** |
| Flare | 4 | 5 | 5 | 2 | 5 | **21** |
| Constella AI | 4 | 5 | 5 | 2 | 5 | **21** |
| LeakRadar | 5 | 5 | 5 | 0 | 3 | **18** |
| NordStellar | 3 | 5 | 0 | 5 | 4 | **17** |
| DeHashed | 4 | 0 | 5 | 0 | 3 | **12** |
| OSINTLeak | 4 | 0 | 5 | 0 | 3 | **12** |
| AmiBreached | 3 | 0 | 5 | 0 | 3 | **11** |
| Have I Been Pwned | 3 | 0 | 5 | 0 | 1 | **9** |
| HackCheck | 3 | 0 | 2 | 0 | 1 | **6** |
| Mozilla Monitor | 3 | 0 | 0 | 0 | 1 | **4** |
| Leaked.domains | 1 | 0 | 0 | 0 | 2 | **3** |
| Leaknix | 1 | 0 | 0 | 0 | 1 | **2** |
| Leak-Lookup | 1 | 0 | 0 | 0 | 1 | **2** |
| DataBreach.com | 1 | 0 | 0 | 0 | 1 | **2** |

---

# Key Insights

### Strongest enterprise + stealer alignment

- **Lunar (25)**
- **SpyCloud (25)**
- **Hudson Rock (24)**


### Strong corpus + automation leaders

- Lunar  
- SpyCloud  
- Intelligence X  
- LeakRadar  
- SOCRadar  

### Strongest session hijack / token detection positioning

- Lunar  
- SpyCloud
- Hudson Rock  
- Breachsense  


---

## Notes & Caveats

- Corpus depth is based on public positioning and claims.
- Session token support is rare and often inconsistently documented.
- API capabilities vary significantly in maturity and accessibility.
- Lookup-only services are not directly comparable to enterprise intelligence platforms.
