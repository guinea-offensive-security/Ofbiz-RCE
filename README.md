# 📌 Apache OFBiz RCE Exploit (CVE-2024-38856)

Ce script Python permet d’exploiter une vulnérabilité de type Remote Code Execution (RCE) sur Apache OFBiz (versions < 18.12.15), via un accès non autorisé à l’endpoint `/webtools/control/forgotPassword/ProgramExport`.

## 🛠️ Description

- **CVE** : CVE-2024-38856
- **Type** : Incorrect Authorization → Remote Code Execution
- **Composant** : Apache OFBiz
- **Versions affectées** : avant 18.12.15
- **Exploit** : Injection de code Groovy converti en Unicode (`\uXXXX`) envoyé via `POST`.

## 🚀 Fonctionnalités

- Exécution de commande Linux à distance (`--cmd`)
- Reverse shell via `busybox`/`nc` (`--shell`)
- Proxy supporté
- Sortie colorée et parsing intelligent de la réponse

## ⚙️ Usage

### 1. Exécution de commande simple

```bash
python3 cve-2024-38856_Scanner.py -u https://TARGET:8443 -c "id"
```
