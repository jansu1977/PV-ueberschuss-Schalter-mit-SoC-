# PV SoC Multi – Home‑Assistant Blueprint & Dashboard

Dieses Repository enthält ein Blueprint, Template‑Sensoren und ein Lovelace‑Dashboard,
um beliebige Shelly‑Steckdosen nach **PV‑Überschuss und Batterie‑SoC** zu steuern.

## Ordnerstruktur

```
blueprints/automation/pv_soc_multi/pv_soc_multi.yaml  # Blueprint
templates/pv_soc_templates.yaml                       # Template‑Sensoren
dashboards/pv_miner_dashboard.yaml                    # Beispiel‑Dashboard
```

## Schnellinstallation

1. **Blueprint importieren**

   ```
   https://my.home-assistant.io/redirect/blueprint_import/?download_url=https://raw.githubusercontent.com/<USER>/<REPO>/main/blueprints/automation/pv_soc_multi/pv_soc_multi.yaml
   ```

   *<USER>/<REPO>* durch deinen GitHub‑Pfad ersetzen.

2. **Automation erstellen**

   * Einstellungen → Automationen & Szenen → Neu → Blueprint verwenden  
   * Blueprint **„PV Überschuss-Schalter mit SoC (Mehrfachgeräte)“** auswählen  
   * Sensoren, Steckdosen & Schwellenwerte setzen.

3. **Dashboard importieren**

   * Dashboards → „+ Dashboard“ → YAML‑Modus →  
     Inhalt aus `dashboards/pv_miner_dashboard.yaml` einfügen.

## Lizenz

MIT – siehe `LICENSE`.
