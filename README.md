# PV SoC Multi – Blueprint & Dashboard

## Inhalt

* **Blueprint** `pv_soc_multi.yaml` – schaltet Shelly-Steckdosen nach PV‑Überschuss & Akku-SoC, inkl. Vorzeichen‑Option
* **Template-Sensoren** `pv_soc_templates.yaml` – erzeugt ausgewählte Sensorwerte & Leistungs­statistiken
* **Lovelace-Dashboard** `pv_miner_dashboard.yaml` – zeigt SoC, Überschuss, Gesamt- & Einzel­verbrauch

## Ordnerstruktur

```
blueprints/automation/pv_soc_multi/pv_soc_multi.yaml
templates/pv_soc_templates.yaml
dashboards/pv_miner_dashboard.yaml
```

## Vorbereitung in Home Assistant

1. **Dateien kopieren** → exakt so unter `/config/` ablegen.
2. **Helpers / Gruppen** anlegen  
   | ID | Typ | Inhalt |
   |----|-----|--------|
   | `input_select.surplus_sensor` | Auswahl | alle Überschuss‑Sensoren |
   | `input_select.battery_soc_sensor` | Auswahl | deine SoC‑Sensoren |
   | `group.miner_switches` | Gerätegruppe | alle Shelly‑Schalter |
   | `group.miner_power_sensors` | Entitätsgruppe | `sensor.<plug>_power` jeder Steckdose |
3. Entwicklerwerkzeuge → YAML  
   * **Blueprints neu laden**  
   * **Vorlagen neu laden**
4. Automation aus Blueprint erstellen.  
   *Schalte „Vorzeichen umkehren“ EIN, wenn dein Sensor bei Einspeisung negative Werte liefert.*
5. Dashboard importieren (YAML-Modus) oder Karten manuell anlegen.

## Lizenz

MIT