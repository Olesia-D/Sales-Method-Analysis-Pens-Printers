# **Vertriebsstrategie-Analyse für "Pens and Printers"**  
Analyse von 3 neuen verschiedenen Vertriebsmethoden  
im Online-Shop für Bürobedarf  

## Projektübersicht  
Dieses Projekt konzentriert sich auf die Analyse neuer Vertriebsmethoden für eine kürzlich eingeführte Produktlinie in einem Online-Schreibwaren-Shop – Pens and Printers. Das Unternehmen, gegründet 1984, bietet eine breite Palette an Bürobedarf von vertrauenswürdigen Herstellern. Da sich das Kaufverhalten der Kunden weiterentwickelt, zielt das Unternehmen darauf ab, Vertriebsstrategien für bessere Effizienz und Rentabilität zu optimieren.  

Dieses Projekt wurde als praktischer Bestandteil  
der Data Analyst-Zertifizierung von DataCamp abgeschlossen.  

## Projektziele  
Bewertung der Wirksamkeit von drei verschiedenen Vertriebsstrategien – Email, Phone Call und Email + Call – die zur Förderung einer neuen Produktlinie für Kreativitäts- und Brainstorming-Tools eingesetzt wurden.  

### Ziele  
- Bereinigung und Vorverarbeitung des Datensatzes mit SQL, Python.  
- Analyse der Verteilung der Kunden insgesamt und für jede Methode, Unterschiede im Umsatz für jede Methode, Festlegung der effektivsten Vertriebsmethode.  
- Visualisierung wichtiger Erkenntnisse, um Trends und Muster aufzudecken.  

## Datensatz-Zusammenfassung  
Datensatz *product_sales* ist hochgeladen  

Der Datensatz besteht aus 15.000 Kundenaufzeichnungen mit Attributen wie:  
- Kunden-ID  
- Vertriebsmethode  
- Umsatz  
- Jahre als Kunde  
- Region  
- Kontaktdatum  

## 🔧 Datenbereinigung & Vorverarbeitung  
Bereinigter Datensatz ist hochgeladen  

### ✔️ Datenvalidierung  
- Datensatz in Google Colab geladen und überprüft.  
- Überprüfung auf fehlende Werte und Ausreißer.  

### ✔️ Behandlung fehlender Umsatzwerte  
- 1.074 fehlende Werte (~7,16 %) in der Umsatzspalte.  
- Annahme: MCAR (Missing Completely At Random).  
- Fehlende Werte durch Mittelwertimputation ausgefüllt.  

### ✔️ Korrektur von Ausreißern  
- Zwei Ausreißer in *years_as_customer* (47 und 63 Jahre).  
- Ersetzt durch 41 (maximal möglicher Wert, basierend auf der Unternehmensgeschichte).  

### ✔️ Standardisierung kategorischer Daten  
- Werte von *sales_method* standardisiert (z. B. 'em + call' → 'Email + Call') für Konsistenz.  

## 📈 Analyse & Visualisierungen  
Analyse durchgeführt und interaktive Dashboards mit Power BI erstellt, einschließlich:  
- Anzahl der Kunden nach Vertriebsmethode  
- Umsatzverteilung  
- Umsatz nach Vertriebsmethode  
- Umsatz im Zeitverlauf nach Methode  

### Wichtige Erkenntnis: Effizienz der Vertriebsmethoden  
- **Vertriebsmethode: Email** (7.466 Kunden, $723.418 Gesamtumsatz, $96,9 ARPC (Durchschnittlicher Umsatz/Kunde))  
- **Vertriebsmethode: Phone Call** (4.962 Kunden, $244.566 Gesamtumsatz, $49,29 ARPC (Durchschnittlicher Umsatz/Kunde))  
- **Vertriebsmethode: Email + Call** (2.572 Kunden, $441.040 Gesamtumsatz, $171,48 ARPC (Durchschnittlicher Umsatz/Kunde))  

- *Email* war am skalierbarsten, aber weniger profitabel pro Kunde.  
- *Email + Call* generierte den höchsten ARPC, was auf starkes Engagement hinweist.  
- *Phone Calls* benötigten die meiste Zeit (30 Min./Kunde), erzielten aber den niedrigsten ARPC.  

## 📐 Metrik für laufende Überwachung  
**Metrik: Durchschnittlicher Umsatz pro Kunde (ARPC) nach Vertriebsmethode**  
**Formel:** ARPC = Gesamtumsatz nach Methode / Anzahl der Kunden in der Methode  

### Warum ARPC?  
- Normalisiert den Umsatz über alle Vertriebsmethoden hinweg.  
- Einfach zu berechnen und zu verfolgen.  
- Ermöglicht aussagekräftige Vergleiche über die Zeit hinweg.  

## 📌 Empfehlungen  
- Priorisierung der Methode "Email + Call" für hochkarätige Kunden aufgrund der höchsten Umsatzeffizienz.  
- Reduzierung oder Abschaffung der "Phone Call"-Strategie – hohe Zeitkosten, geringe Rendite.  
- Verbesserung der Email-Kampagnen – anfängliche Ergebnisse waren stark, aber die Effektivität nahm im Laufe der Zeit ab. Untersuchung und Optimierung erforderlich.  

## 🛠️ Verwendete Tools  
- DBeaver (SQL) – für Datenbereinigung, Vorverarbeitung und Analyse  
- Google Colab (Python (Pandas, NumPy, Matplotlib)) – für Datenbereinigung, Vorverarbeitung und Analyse  
- Power BI (für interaktive Dashboards)  
- GitHub (für Versionskontrolle)  

## 📁 Ordnerstruktur  
├── product_sales.csv # Originaldatensatz  
├── cleaned_product_sales.csv # Rohe und bereinigte Datensätze  
├── Practical_Exam_DataCamp.ipynb # Jupyter/Colab-Analysedateien  
├── visuals/ Customers_by_approach.png # Screenshots oder Berichte aus Power BI  
├── Overall_Revenue_Distribution.png  
├── Revenue_by_sales_method.png  
├── Revenue_by_week_and_method.png  
├── Presentatation Product Sales.pdf # Übersichtspräsentation für den Leiter der Analytik  
├── README.md # Projektübersicht  

## 🚀 Zukünftige Arbeit  
- Automatisierung von Dashboard-Updates über Cloud-Datenpipelines.  
- Einbindung von A/B-Tests für neue Vertriebsmethoden.  
- Weitere Segmentierung der Kunden nach Region oder Branche.  
