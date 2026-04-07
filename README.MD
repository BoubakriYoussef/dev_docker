# TP1 - Fondamentaux Cloud & GCP

**Étudiant :** Boubakri Youssef

## 🚀 Réalisations

### 1. Infrastructure GCP
- **Configuration :** `gcloud` configuré en `europe-west9`.
- **Storage :** Bucket créé en classe de stockage STANDARD.
- **Compute :** Instance `tp1-vm` créée, testée via SSH, puis supprimée.

### 2. Conteneurisation (Docker)
- **Application :** Flask (Python 3.12).
- **Build :** `docker build -t tp1-flask:v1 .`
- **Stats :** Consommation RAM au repos ~25 MiB.

## 📸 Preuves en images
Toutes les captures sont disponibles dans le dossier `/screenshots` :
- `buckets list.png` : État du stockage GCS.
- `creation vm.png` / `suppression vm.png` : Cycle de vie de la VM.
- `ssh.png` : Connexion réussie à l'instance.
- `accountservice.png` : Configuration du Service Account.

## 🧠 Réponses clés
- **Sécurité :** On n'utilise pas le rôle `Owner` pour un Service Account afin d'appliquer le **principe du moindre privilège**.
- **Dockerfile :** On copie `requirements.txt` avant le code pour optimiser le **cache des layers** Docker.
- **NIST :** Les 5 piliers sont : Self-service, Large accès réseau, Mutualisation, Élasticité, Service mesuré.