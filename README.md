# Orchestration Automatique — Cluster Kubernetes
Conception et déploiement d’une chaîne complète d’automatisation d’infrastructure, du provisionnement de VM jusqu’au test de bout en bout.

▸ Cluster Kubernetes de 3 nœuds (1 master, 2 workers) virtualisé sur Proxmox
▸ Hébergement des outils CI/CD dans un namespace dédié : serveur Git Gitea et serveur Jenkins
▸ Infrastructure as Code avec Terraform : création d’une VM et d’un conteneur sur Proxmox, gestion complète du cycle de vie (apply / destroy)
▸ Configuration automatisée avec Ansible : installation de Nginx, idempotence du playbook vérifiée
▸ Pipeline Jenkins multibranche déclenché automatiquement à chaque git push : Terraform crée la VM → Ansible installe Nginx → Docker déploie le reverse proxy → test curl de bout en bout

Stack : Proxmox · Kubernetes · Terraform · Ansible · Jenkins · Gitea · Docker · Nginx
