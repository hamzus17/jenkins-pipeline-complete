 🚀 DevOpsProject2 – CI/CD avec Docker, Jenkins, SonarQube, Prometheus et Grafana

📌 Description

Ce projet illustre la mise en place d’un **pipeline CI/CD complet** pour une application web.
L’objectif est d’automatiser **les tests, le build, le déploiement** et d’assurer la **supervision** via un ensemble d’outils DevOps.

---

⚙️ Outils utilisés

* **Jenkins** : orchestration CI/CD
* **GitHub** : gestion du code source
* **SonarQube** : analyse qualité et sécurité du code
* **Docker & DockerHub** : conteneurisation et registre d’images
* **AWS EC2 (Ubuntu)** : déploiement de l’application
* **Prometheus + Grafana** : monitoring et visualisation

---

🛠️ Pipeline CI/CD

Le pipeline est défini dans le fichier `Jenkinsfile` et se compose des étapes suivantes :

1. **Checkout** : Récupération du code source depuis GitHub.
2. **Build & Test** : Installation des dépendances et exécution des tests.
3. **Analyse SonarQube** : Vérification de la qualité du code.
4. **Build Docker** : Création de l’image Docker.
5. **Push DockerHub** : Envoi de l’image vers DockerHub.
6. **Déploiement EC2** : Déploiement automatique sur une instance AWS.
7. **Monitoring** : Supervision via Prometheus et Grafana.


---

## 🖼️ Architecture du projet


```
Dev → GitHub → Jenkins → SonarQube + Docker Build → DockerHub → EC2 → Prometheus & Grafana
```

---

## 🔍 Monitoring

* **Prometheus** : collecte les métriques depuis l’EC2 et les conteneurs.
* **Grafana** : visualisation via des dashboards.

Endpoints utiles :

* Prometheus : `http://<EC2-IP>:9090`
* Grafana : `http://<EC2-IP>:3000`

---

## 📦 Déploiement

Après un push sur la branche `main` :

* Jenkins exécute le pipeline.
* Une nouvelle image Docker est générée et publiée sur DockerHub.
* L’application est déployée automatiquement sur EC2 avec `docker run`.



## ✅ Résultats attendus

* Une application web accessible via `http://<EC2-IP>`
* Pipeline CI/CD automatisé et fonctionnel
* Qualité du code vérifiée avec SonarQube
* Supervision en temps réel avec Grafana

---

## 👨‍💻 Auteur

Projet réalisé par **Argoubi Hamza** – Étudiant ingénieur DevOps


