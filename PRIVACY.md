
# Privacy Policy & Data Sovereignty (DSGVO / GDPR) — AI Token & Cost Tracker

**Author / Controller:** Vladyslav Vitko

---

## 1. Local-First Data Architecture (100% Local Processing)

**AI Token & Cost Tracker** is engineered as a **100% Local-First** developer utility and proxy gateway (`http://127.0.0.1:8787`):

1. **Zero Cloud Telemetry:** The extension and local Python daemon do **not** collect, transmit, or store any usage analytics, crash reports, prompts, completions, source code, or repository names on any server controlled by Vladyslav Vitko.
2. **Local SQLite Storage:** All token counters, request metadata, and project cost ledgers are stored strictly on your local disk (`~/.config/ai-token-tracker/usage.sqlite3` or the local `data/usage.sqlite3` folder).
3. **Isolated API Keys (`chmod 0600`):** Your upstream LLM provider API keys (Google Gemini, Anthropic Claude, OpenAI, OpenRouter, or custom endpoints) are stored exclusively on your local filesystem (`secrets.json` with strict `0600` POSIX owner-only permissions) and are transmitted only directly from your machine to the respective upstream LLM provider you explicitly invoke.

---

## 2. License Key Validation & Merchant of Record (Pro / Team Tier)

- **Free Community Edition & Offline Keys (`AITT1-...`):** Operate completely offline with zero external network requests for licensing.
- **Online Pro/Team License Keys (Polar.sh / Lemon Squeezy):** When you activate an online license key or when recurring subscriptions (Monthly / Annual) periodically verify renewal status, your local daemon sends a direct HTTPS request containing strictly the license key string and an anonymized local instance identifier (`hostname-ide`) to the Merchant of Record API (`api.polar.sh` or `api.lemonsqueezy.com`) to verify active billing validity. No prompts, source code, project names, or usage metrics are ever included in license verification requests.
- Payment processing, invoicing, and VAT/MwSt compliance are handled exclusively by the Merchant of Record (Polar.sh or Lemon Squeezy) under their respective GDPR-compliant privacy policies.

---

## 3. Datenschutzerklärung (Deutsch — DSGVO)

### 3.1 Grundsatz: 100% Lokale Datenverarbeitung

**AI Token & Cost Tracker** arbeitet vollständig lokal auf Ihrem Endgerät (`127.0.0.1:8787`). Weder Prompts noch Antworten, Quellcode, Projektnamen oder API-Schlüssel werden an den Entwickler (**Vladyslav Vitko**) übertragen.

### 3.2 Lokale Speicherung

- **Datenbank:** Alle Token- und Kostenstatistiken werden ausschließlich lokal in einer SQLite-Datenbank (`usage.sqlite3`) auf Ihrem Computer gespeichert.
- **API-Schlüssel:** Ihre hinterlegten Provider-API-Keys werden lokal mit strikten Dateiberechtigungen (`chmod 0600`) in `secrets.json` gespeichert und nur bei expliziten API-Aufrufen direkt an den jeweiligen KI-Anbieter (Google, Anthropic, OpenAI, OpenRouter etc.) übermittelt.

### 3.3 Lizenzprüfung & Zahlungsabwicklung

- Bei Nutzung von Offline-Lizenzschlüsseln (`AITT1-PRO-...`) findet keinerlei externe Kommunikation statt.
- Bei Aktivierung oder periodischer Verlängerungsprüfung (Auto-Renewal bei Monats- oder Jahresabonnements) eines über unseren Zahlungsabwickler (Merchant of Record: **Polar.sh** oder **Lemon Squeezy**) erworbenen Lizenzschlüssels wird ausschließlich der Lizenzschlüssel sowie eine lokale Instanz-Kennung zur Gültigkeitsbestätigung per HTTPS an die API des jeweiligen Zahlungsabwicklers übermittelt (Rechtsgrundlage: Art. 6 Abs. 1 lit. b DSGVO — Vertragserfüllung). Es werden zu keinem Zeitpunkt Projektdaten, Quellcodes, Prompts oder Nutzungsstatistiken übertragen.

### 3.4 Ihre Rechte nach DSGVO

Da sämtliche Nutzungsdaten ausschließlich lokal auf Ihrem eigenen Gerät gespeichert werden, haben Sie jederzeit die volle Kontrolle über Ihre Daten und können diese jederzeit durch Löschen der lokalen Datei `usage.sqlite3` bzw. `secrets.json` vollständig entfernen.
