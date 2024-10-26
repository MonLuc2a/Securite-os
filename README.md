---

# Script de durcissement pour Fedora

Ce script bash renforce la sécurité d’un système Fedora en appliquant diverses configurations de durcissement, notamment sur les permissions, la configuration des mots de passe, les services réseau, et le pare-feu. Après exécution, le système atteint un score de sécurité **Lynis de 79**.

## Fonctionnalités

- Renforcement des permissions sur les fichiers de planification des tâches (cron).
- Application de politiques strictes de mot de passe.
- Activation et configuration de `firewalld` avec une politique par défaut restrictive.
- Installation et configuration de **Fail2Ban** pour protéger contre les tentatives de connexion non autorisées.
- Configuration de SSH pour désactiver l'accès root et l'authentification par mot de passe.
- Installation d'outils de sécurité : **Lynis**, **rkhunter**, **ClamAV**, **usbguard**.
- Désactivation des services inutiles pour réduire la surface d'attaque.
- Application de réglages sysctl pour durcir la sécurité du noyau.
- Désactivation des modules de noyau non nécessaires.

## Utilisation

1. Téléchargez le script et donnez-lui les droits d'exécution :
   ```bash
   chmod +x hardening-fedora.sh
   ```

2. Exécutez le script avec des privilèges root :
   ```bash
   sudo ./hardening-fedora.sh
   ```

3. Redémarrez le système pour appliquer les modifications.

## Résultat

Après l’exécution, le système est renforcé avec un **score de sécurité Lynis de 79**.
