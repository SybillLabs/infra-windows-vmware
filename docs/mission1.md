<h1 align="center">
    🛠️ Préparer la plateforme de virtualisation
</h1>

## `> quickstart`
- Configurer le réseau interne VMnet2 pour le LAN `192.168.99.0/24`.
- Configurer le réseau interne VMnet8 pour le WAN/NAT.
- Configurer les machines virtuelles.
- Utilisation de **snapshot** comme moyen de récupération.

## `> the_needs`

| VMs            | vCPU | RAM      | Disques        | OS                  |
| -------------- | ---- | -------- | -------------- | ------------------- |
| **SRV-DC01**   | 2    | 4 Go     | 60 Go Systèmes | Windows Server 2025 |
|                |      |          | 20 Go Données  |                     |
| **SRV-DC02**   | 2    | 4 Go     | 60 Go Systèmes | Windows Server 2025 |
| **SRV-RTR01**  | 2    | 2 à 4 Go | 50 Go Systèmes | Windows Server 2025 |
| **CLI-W11-xx** | 2    | 4 Go     | 64 Go Systèmes | Windows 11          |

## `> F.A.Q`
- **_Pourquoi VMware Workstation est considéré comme un hyperviseur de type 2 ?_**  
    Car **VMware Workstation** a besoin d'être installé sur un système d'exploitation hôte comme _Windows 11_ ou _Linux_.  
    Contrairement à **Proxmox** qui est de type 1, et est installé en bare metal (pas de système d'exploitation hôte).
- **_Quel est la différence entre NAT, réseau interne(Host-Only) et mode Bridge ?_**  
    - **Mode NAT** : La machine virtuelle accède à Internet en se masquant derrière l'adresse IP de l'ordinateur hôte, qui agit alors comme un routeur intermédiaire pour traduire ses requêtes.
    - **Mode réseau interne (_Host-Only_)** : La machine virtuelle est placée dans un réseau privé totalement isolé d'Internet, où elle peut uniquement communiquer avec les autres machines virtuelles de ce réseau et avec l'ordinateur hôte.
    - **Mode bridge (_Accès par pont_)** : La machine virtuelle est connectée directement au réseau physique de l'hôte et obtient sa propre adresse IP auprès de votre box ou routeur réel, se comportant comme un ordinateur physique distinct.
- **_Quel est l'utilité d'un snapshot ?_**  
    Un **snapshot** permet de sauvegardé la machine virtuelle à un état précis pour que si jamais la machine virtuelle est cassée, il y a possibilité de revenir en arrière.  
    Par exemple, sur **SRV-DC01**, j'installe le service _DHCP_ mais dans le processus je casse **SRV-DC01**. La machine virtuelle n'est pas perdue car j'ai pensé à faire un snapshot avant d'installer le service _DHCP_.   
    J'utilise ce snapshot pour relancer **SRV-DC01** avant que je ne casse la machine virtuelle.  
    Et comme tous les snapshot sont sauvegardés, cela permet d'avoir aussi un historique de ce qui a été fait sur la machine virtuelle.
> **Note** : Un snapshot n'est pas un bacpup, si le disque dur de l'hôte plante, la machine virtuelle est perdue à jamais.
- **_Quel est la différence entre la carte réseau physique de l'hôte et les cartes virtuelles des machines virtuelles ?_**
    Les **cartes virtuelles** ne peuvent pas envoyer de données sur le vrai réseau seules, elles doivent obligatoirement passer par un **commutateur virtuel** (comme _VMnet2_ ou _VMnet8_).  
    Ces commutateurs s'appuie sur la **carte physique** de l'hôte pour transmettre les paquets vers l'extérieur lorsque cela est nécessaire.

---

<p align="center">  
    <i>↪️ Back to<a href="https://github.com/SybillLabs/infra-windows-vmware.git"> Infrastructure Windows avec VMware</a></i>
</p>