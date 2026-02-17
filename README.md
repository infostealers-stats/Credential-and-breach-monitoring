
# Breach / Stealer-Log / Identity Exposure Services Comparison (with Scoring)

This document compares a set of breach intelligence, dark web monitoring, and identity exposure services across five practical dimensions:

- **Breach corpus depth** (how large their searchable breach dataset is)
- **Stealer-log access** (whether they explicitly support infostealer-derived data)
- **API availability** (documented programmatic access)
- **Session token / cookie support** (explicit coverage of live authentication secrets)
- **Core positioning** (what the product is primarily marketed as)

The goal is not to crown a “winner”, but to create a practical map of the market for anyone evaluating vendors for:
- breach intelligence enrichment
- identity exposure monitoring
- infostealer-driven compromise detection
- automation and integration into SOC workflows

---

## Comparison Table (Raw)

| Service | Link | Breach corpus depth | Stealer-log access | API | Session token/cookie | Core positioning |
|---|---|---:|---|---|---|---|
| Intelligence X | https://intelx.io/ | XL | Yes* | Yes | Possible (not explicit) | Breach search / OSINT |
| Have I Been Pwned | https://haveibeenpwned.com/ | M | No | Yes | No | Consumer/Domain leak alerts |
| SOCRadar | https://socradar.io/ | L | Yes | Yes | Likely (not explicit) | Digital risk / dark web |
| SpyCloud | https://spycloud.com/ | L | Yes | Yes | Possible (not documented) | Enterprise identity risk |
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
A high-level rating based on public positioning and credible corpus claims.

- **XL**: Claims of hundreds of billions of records  
- **L**: Tens of billions or significant corpus claims  
- **M**: Mid-range corpus (millions to low billions)  
- **Unknown**: No credible public corpus claim found  

### Stealer-log access
Marked **Yes** only if the company explicitly states support for **infostealer logs** or similar sources (malware-exfiltrated dumps, stealer dumps, session/cookie theft, etc.).

### API availability
Includes commercial APIs and/or documented programmatic access for search and alerts.

### Session token/cookie support
Tracked only where a vendor publicly mentions monitoring:
- session tokens  
- cookies  
- bearer tokens  
- authentication secrets  
- “session hijack” artifacts  

### Core positioning
Whether breach monitoring/search is the primary product, vs. a smaller module inside a broader security platform.

---

## Vendor Summaries (What the Table Actually Means)

### Intelligence X
A broad OSINT + data indexing platform that supports searching across leaks, darknet content, and archived datasets. It is used heavily for investigation workflows and deep breach research. The corpus is among the largest in the space, and it provides an API, though “token/cookie monitoring” is not typically positioned as a first-class feature.

### Have I Been Pwned (HIBP)
The most consumer-friendly and widely trusted breach alert service. It focuses on known breach events and notifications, not stealer logs or advanced threat intel. It provides API access, but the product is intentionally conservative and privacy-minded compared to dark web intelligence vendors.

### SOCRadar
A digital risk and external threat intelligence platform with broad monitoring across open/deep/dark web. It tends to serve SOC and threat intel teams rather than being a pure “breach search engine.” It explicitly includes dark web signals and likely includes stealer-derived sources, although session token handling is not always clearly documented.

### SpyCloud
An enterprise identity exposure and account takeover prevention vendor. It heavily focuses on breach data and malware-derived exposure, including stealer logs. SpyCloud is positioned more as a defensive identity risk platform than as a general OSINT search engine.

### DeHashed
A breach search engine that supports lookups across common identifiers (emails, usernames, domains, IPs). It is widely used by analysts for breach enrichment and verification. It provides API access but is not typically marketed as a stealer-log-first platform, and token/cookie support is not public.

### AmiBreached
A breach monitoring product focused on identity exposure alerts. It is less about investigation depth and more about detection/notification. It provides an API but does not strongly position itself around stealer logs or authentication token monitoring.

### KELA
A cybercrime intelligence platform focused on underground ecosystems: forums, marketplaces, actors, and data leaks. It has strong stealer-log and identity exposure relevance, but is positioned as a broader threat intel vendor rather than a breach lookup tool.

### OSINTLeak
An OSINT-driven leak search/monitoring service. It is closer to breach lookup and alerting than to full threat intel. API access exists, but stealer logs and session token support are not emphasized.

### Hudson Rock
A stealer-log-first service strongly associated with infostealer intelligence. It is one of the clearest vendors in the space for connecting stealer infections to exposed credentials and active session artifacts, and it explicitly supports session token/cookie exposure.

### Flare
A dark web threat intelligence platform designed for continuous monitoring and alerting. It covers a broad range of underground signals including leaked credentials and likely stealer-derived datasets. Token/cookie support may exist but is not consistently explicit.

### NordStellar
A newer entrant positioned specifically around dark web monitoring with strong marketing emphasis on cookies/session hijacking. It is one of the few vendors that explicitly highlights session token/cookie alerts, but API access is not a primary offering.

### Breachsense
A monitoring platform focused on breached credentials and dark web exposures. It is notable for explicitly mentioning session tokens/cookies, which is rare. It also supports stealer logs and API access.

### LeakRadar
A large-scale breach search platform with strong corpus claims and API access. It is positioned as a breach intelligence source with large coverage, and is one of the strongest “corpus + API” combinations. Explicit session token/cookie monitoring is not clearly documented.

### HackCheck
A breach lookup service that is primarily portal-based. It is accessible and consumer-friendly, but it does not appear to support stealer logs or session token monitoring.

### Constella AI
An identity intelligence vendor that combines breach + stealer exposure into an enterprise identity risk perspective. It is closer to SpyCloud in positioning than to a generic breach search engine. Token/cookie support may exist in practice, but is not consistently documented publicly.

### Mozilla Monitor
A consumer breach alerting service built around Have I Been Pwned data. It is designed for usability and remediation, not for threat intelligence or investigation. It does not offer API access or stealer-log support.

### Lookup-Only Utilities (Leaknix, Leak-Lookup, DataBreach.com, Leaked.domains)
These platforms provide basic breach lookup capabilities by scanning known breach datasets and listing whether an email or domain appears in compromises. They may be useful for quick checks, but generally do not offer stealer-log depth, API integrations, or advanced identity risk workflows.

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
- Partial / portal-only / unclear = 2  
- No = 0  

### 4) Session token/cookie monitoring (0–5)
- Yes = 5  
- Possible / likely / unclear = 2  
- No = 0  

### 5) Enterprise positioning (0–5)
- Enterprise cyber intel / identity risk / threat intel platform = 5  
- Mixed (prosumer or SMB, breach lookup + monitoring) = 3  
- Consumer lookup/alerts = 1  

> Note: This scoring is not a “best product” ranking.  
> It is a practical score for enterprise breach + stealer intelligence value, biased toward automation and high-signal data.

---

## Scored Table

| Service | Corpus (0–5) | Stealer (0–5) | API (0–5) | Tokens (0–5) | Enterprise (0–5) | Total (0–25) |
|---|---:|---:|---:|---:|---:|---:|
| Intelligence X | 5 | 5 | 5 | 2 | 4 | **21** |
| Have I Been Pwned | 3 | 0 | 5 | 0 | 1 | **9** |
| SOCRadar | 4 | 5 | 5 | 2 | 5 | **21** |
| SpyCloud | 4 | 5 | 5 | 2 | 5 | **21** |
| DeHashed | 4 | 0 | 5 | 0 | 3 | **12** |
| AmiBreached | 3 | 0 | 5 | 0 | 3 | **11** |
| KELA | 4 | 5 | 5 | 2 | 5 | **21** |
| OSINTLeak | 4 | 0 | 5 | 0 | 3 | **12** |
| Hudson Rock | 4 | 5 | 5 | 5 | 5 | **24** |
| Flare | 4 | 5 | 5 | 2 | 5 | **21** |
| NordStellar | 3 | 5 | 0 | 5 | 4 | **17** |
| Breachsense | 3 | 5 | 5 | 5 | 4 | **22** |
| Leaknix | 1 | 0 | 0 | 0 | 1 | **2** |
| Mozilla Monitor | 3 | 0 | 0 | 0 | 1 | **4** |
| LeakRadar | 5 | 5 | 5 | 0 | 3 | **18** |
| HackCheck | 3 | 0 | 2 | 0 | 1 | **6** |
| Constella AI | 4 | 5 | 5 | 2 | 5 | **21** |
| Leak-Lookup | 1 | 0 | 0 | 0 | 1 | **2** |
| Leaked.domains | 1 | 0 | 0 | 0 | 2 | **3** |
| DataBreach.com | 1 | 0 | 0 | 0 | 1 | **2** |

---

## Score-Based Insights

### Top overall (enterprise + stealer + automation)
These are the strongest matches for modern identity compromise workflows:

- **Hudson Rock (24)**
- **Breachsense (22)**
- **SpyCloud / SOCRadar / KELA / Flare / Constella AI / Intelligence X (21)**

### Best “big corpus + API” options
If your priority is a large searchable dataset with programmatic access:

- **Intelligence X**
- **LeakRadar**
- **SpyCloud**
- **SOCRadar**

### Best “session hijack / token” positioning
Explicit session token/cookie monitoring is rare. The strongest signals here are:

- **Hudson Rock**
- **Breachsense**
- **NordStellar**

### Best consumer alerting (not enterprise intel)
Strong for individuals and domains, but not stealer-log or SOC integration tools:

- **Have I Been Pwned**
- **Mozilla Monitor**

---

## Notes & Caveats

- **Corpus depth is tricky.** Vendors define “records” differently (plaintext vs hashed, unique vs raw dumps). Corpus estimates here are high-level.
- **Session token support is rare.** Most breach monitoring vendors focus on credentials and PII; explicit token/cookie monitoring is found only in a handful of services.
- **API public documentation varies.** Some offer robust APIs with keys and endpoints, others have limited or partner-only access.
- **Some names are search-only.** Leaknix, Leak-Lookup, DataBreach.com, and Leaked.domains are typically lookup tools with limited advanced signals.



