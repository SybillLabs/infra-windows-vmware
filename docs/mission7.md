<h1 align="center">
    📁 Mettre en place les ressources de fichiers
</h1>

## `> quickstart`
- Définir les permissions de partage et NTFS cohérentes respectant l'**AGDLP**.
- Le groupe `GL_IT` doit disposer des droits nécessaires pour administrer les ressources de fichiers.
- Installation de FSRM et limitation de chaque répertoire à **200 Mo**.
- Générer un avertissement lorsque l'utilisation atteint **160 Mo**.

## `> control_point`
### 1. Permissions de partage et NTFS pour *Direction*  
![srv-dc01_permission-direction](/screenshots/srv-dc01_permission-direction.png)

### 2. Permissions de partage et NTFS pour *Gestion*  
![srv-dc01_permission-gestion](/screenshots/srv-dc01_permission-gestion.png)

### 3. Permissions de partage et NTFS pour *Informatique*  
![srv-dc01_permission-informatique](/screenshots/srv-dc01_permission-informatique.png)

### 4. Application du rôle FSRM avec limitation et avertissement sur chaque répertoire
![srv-dc01_fsrm](/screenshots/srv-dc01_fsrm.png)

---

<p align="center">  
    <i>↪️ Back to<a href="https://github.com/SybillLabs/infra-windows-vmware.git"> Infrastructure Windows avec VMware</a></i>
</p>