# LAB-7-Analyse-Dynamique-Mobile-avec-MobSF
# 🧪 LAB 7 : Analyse Dynamique Avancée d'applications Mobiles avec MobSF

## 📝 Description du Projet
Ce laboratoire est dédié à l'**analyse dynamique automatisée** d'un fichier APK. Contrairement à l'analyse statique, l'analyse dynamique consiste à exécuter l'application dans un environnement contrôlé (Émulateur/Sandbox) pour observer son comportement en temps réel, intercepter les flux réseau, analyser la mémoire et manipuler l'exécution à l'aide d'outils d'instrumentation comme **Frida**.

---

## 🛠️ Outils & Environnement de Test
* **Framework principal :** Mobile Security Framework (MobSF) - Dynamic Analyzer
* **Environnement virtuel :** VM Mobexle
* **Instrumentation dynamique :** Frida Scripting Integration
* **Émulateur cible :** Genymotion / Android Runtime intégré

---

## 📸 Étapes d'Exécution et Captures du Lab

### Étape 1 : Initialisation de l'analyseur dynamique
Lancement de l'environnement de test et configuration de la communication entre MobSF et l'émulateur Android. Le framework se prépare à surveiller le cycle de vie de l'application.
<img width="1116" height="220" alt="Initialisation dynamic analyzer MobSF" src="https://github.com/user-attachments/assets/295dde51-64b6-4d8c-9c88-241dad6cf105" />

### Étape 2 : Lancement de l'APK dans la Sandbox
L'application cible est installée et exécutée automatiquement sur l'émulateur connecté. MobSF commence à capturer l'activité du système et l'interface utilisateur.
<img width="1342" height="552" alt="Lancement de l'application sur l'émulateur" src="https://github.com/user-attachments/assets/869227d9-be37-4d98-8215-5ebb852acbca" />

### Étape 3 : Capture de l'activité de l'application
Suivi des composants Android activés (Activities, Services, Broadcast Receivers) lors de l'interaction avec l'application.
<img width="1418" height="435" alt="Capture d'activité Android" src="https://github.com/user-attachments/assets/f5b08aa7-589b-4fe0-8ddc-112bf4f2e178" />

### Étape 4 : Instrumentation dynamique avec les scripts Frida
Sélection et injection de scripts Frida personnalisés via l'interface de MobSF pour réaliser des opérations avancées (Bypass de SSL Pinning, Root Detection bypass, ou interception de fonctions cryptographiques).
<img width="1475" height="644" alt="Injection de scripts Frida" src="https://github.com/user-attachments/assets/d60118c0-8568-401e-b386-a10c0641f484" />

### Étape 5 : Exécution du script de test
Confirmation du bon fonctionnement de l'agent Frida injecté au sein du processus de l'application cible.
<img width="537" height="67" alt="Statut de l'exécution du script" src="https://github.com/user-attachments/assets/fb1e490d-c5b7-4e47-a313-22c81f98fec6" />

### Étape 6 : Interception et Analyse des Logs (Logcat)
Visualisation globale et filtrage des journaux d'événements (Android Logcat) générés par l'application pour extraire d'éventuelles informations sensibles (clés API, identifiants, tokens).
<img width="1919" height="1076" alt="Analyse détaillée des logs système" src="https://github.com/user-attachments/assets/71a01337-e751-4cf4-8339-6e9f3b4af173" />

### Étape 7 : Analyse des fichiers créés en mémoire locale
Vérification du stockage local de l'application (SharedPreferences, bases de données SQLite). L'objectif est de vérifier si des données sensibles sont stockées en clair dans le répertoire `/data/data/`.
<img width="1582" height="346" alt="Audit du stockage local" src="https://github.com/user-attachments/assets/155bb8aa-7788-426d-901d-c2f752ecbbf4" />

### Étape 8 : Interception du trafic réseau (HTTP/HTTPS)
Analyse des requêtes et réponses HTTP générées par l'APK afin de vérifier la sécurité des communications avec le serveur distant et s'assurer de l'absence de fuite de données privées.
<img width="1575" height="506" alt="Analyse du trafic réseau" src="https://github.com/user-attachments/assets/b27581b7-5e03-43d2-b7e7-43ab11ef363c" />

### Étape 9 : Génération du rapport de sécurité dynamique final
Compilation de l'ensemble des comportements suspects identifiés durant l'exécution, classés par niveau de sévérité pour finaliser l'audit de sécurité.
<img width="1551" height="654" alt="Rapport d'analyse dynamique final" src="https://github.com/user-attachments/assets/5f4a3d9e-1593-4a10-bf6a-4644fd294e3c" />

---

## 📌 Points clés à retenir
1. **Complémentarité :** L'analyse dynamique permet de découvrir des failles qui restent invisibles lors de l'analyse statique (ex: comportements déclenchés uniquement lors de l'exécution, chiffrement à la volée).
2. **Puissance de Frida :** L'intégration de Frida dans MobSF facilite grandement le reverse engineering en permettant de modifier le comportement de l'application sans avoir à la recompiler.
