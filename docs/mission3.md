<h1 align="center">
    🚀 Déployer le premier contrôleur de domaine
</h1>

## `> quickstart`
- Installer et configurer `Active Directory Domain Services` sur **SRV-DC01**.
- Configurer le `DNS` sur **SRV-DC01**.
- Configurer le routage sur **SRV-RTR01**.

## `> control_point`
### 1. **SRV-DC01** en contrôleur de domaine  
![srv-dc01_adds](/screenshots/srv-dc01_adds.png)

### 2. **SRV-DC01** avec DNS opérationnel  
![srv-dc01_dns-up](/screenshots/srv-dc01_dns-up.png)

### 3. Test de résolution de nom depuis **SRV-DC02**  
![srv-dc02_dns-test](/screenshots/srv-dc02_test-dns.png)

### 4. Résolution DNS vers Internet depuis **SRV-DC01**

- Source : [IT-Connect : Comment configurer Windows Server 2025 comme routeur avec du NAT ?](https://www.it-connect.fr/comment-configurer-windows-server-2025-comme-routeur-avec-nat/)

![srv-dc01_dns-wan](/screenshots/srv-dc01_dns-wan.png)

---

<p align="center">  
    <i>↪️ Back to<a href="https://github.com/SybillLabs/infra-windows-vmware"> Infrastructure Windows avec VMware</a></i>
</p>