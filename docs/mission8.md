<h1 align="center">
    📑 Déployer les stratégies de groupe
</h1>

## `> quickstart`
- Mettre en œuvre ces cinq stratégies :

| GPO                       | Objectif                                                                              | Cible / Remarque                                                  |
| ------------------------- | ------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| Verrouillage automatique  | Verrouiller la session après 10 minutes d'inactivité                                  | Utilisateurs du domaine                                           |
| Politique de mot de passe | Longueur minimale de 12 caractères, complexité activée, historique de 5 mots de passe | Politique appliquée au niveau du domaine                          |
| Panneau de configuration  | Interdire l'accès au Panneau de configuration et aux Paramètres Windows               | Uniquement l'OU Test-GPO                                          |
| Lecteurs réseau           | Mapper automatiquement les lecteurs correspondant au service de l'utilisateur         | Utiliser les groupes et/ou les préférences de stratégie de groupe |
| Fond d'écran entreprise   | Appliquer un fond d'écran commun depuis un emplacement réseau accessible en lecture   | Tester avec au moins un utilisateur du domaine                    |

## `> control_point`
### 1. Verrouillage automatique  
![srv-dc01_verrouillage-écran](/screenshots/srv-dc01_verrouillage-écran.png)

### 2. Politique de mot de passe
![srv-dc01_politique-motdepasse](/screenshots/srv-dc01_politique-motdepasse.png)

### 3. Panneau de configuration
![srv-dc01_configpanel-parameters](/screenshots/srv-dc01-configpannel-parameters.png)

### 4. Lecteurs réseau (*identique pour chaque dossier*)
![srv-dc01_lecteur-reseau](/screenshots/srv-dc01_lecteur-reseau.png)
![cli-w11-01_lecteur-reseau](/screenshots/cli-w11-01_lecteur-reseau.png)

### 5. Fond d'écran entreprise  
![srv-dc01_fond-écran](/screenshots/srv-dc01_fond-écran.png)
![cli-w11-01_fond-écran](/screenshots/cli-w11-01_fond-écran.png)

### 6. Test-GPO
![cli-w11-01_test-gpo](/screenshots/cli-w11-01_test-gpo.png)

---

<p align="center">  
    <i>↪️ Back to<a href="https://github.com/SybillLabs/infra-windows-vmware.git"> Infrastructure Windows avec VMware</a></i>
</p>