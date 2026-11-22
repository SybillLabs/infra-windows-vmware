<h1 align="center">
    🔁 Ajouter SRV-DC02 et vérifier la réplication
</h1>

## `> quickstart`
- Joindre **SRV-DC02** au domaine `ais.test`.
- Installer les rôles `AD-DS` et `DNS` puis le promouvoir comme contrôleur de domaine supplémentaire.
- Vérifier la réplication avec les outils adaptés (*ADUC* ou *DNS Manager* ou *REPADMIN*)

## `> control_point`
### 1. Vue de la réplication de **SRV-DC01** vers **SRV-DC02** depuis **SRV-DC01** avec `repadmin`  
![srv-dc01_repadmin](/screenshots/srv-dc01_repadmin.png)

### 2. Vue de la réplication de **SRV-DC01** vers **SRV-DC02** depuis **SRV-DC02** avec `repadmin`  
![srv-dc02_repadmin](/screenshots/srv-dc02_repadmin.png)

### 3. Test de réplication en live avec l'`Active Directory Users and Computers`
![srv-dc02_aduc](/screenshots/srv-dc02_aduc.png)

### 4. Vérification d'aucune changement des rôles FSMO depuis **SRV-DC01**  
![srv-dc01_fsmo](/screenshots/srv-dc01_fsmo.png)

---

<p align="center">  
    <i>↪️ Back to<a href="https://github.com/SybillLabs/infra-windows-vmware.git"> Infrastructure Windows avec VMware</a></i>
</p>