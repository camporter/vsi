---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

keywords: public virtual servers, network traffic, virtual server deployment

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# A propos des serveurs virtuels publics
{: #about-public-virtual-servers}

Les offres des serveurs {{site.data.keyword.BluVirtServers}} publics sont des déploiements de serveur virtuel à service partagé gérés par IBM. Elles offrent une évolutivité rapide et une meilleure rentabilité avec des tailles prédéfinies répondant à vos besoins métier pour que vous soyez opérationnel rapidement.  
{:shortdesc}

Les serveurs virtuels publics présentent un grand nombre d'avantages, notamment les suivants :

* **Disponibilité globale**

    L'offre de serveur virtuel est disponible dans les centres de données du monde entier.

* **Choix de configuration, déploiement rapide et évolutivité**

    L'offre de serveur virtuel public propose des options de serveur virtuel de grande ou petite taille permettant de répondre à vos différentes exigences de charge de travail.

Le trafic réseau pour les serveurs virtuels publics, qui englobe le VSI SAN et d'autres systèmes de stockage en réseau, n'offre pas de garantie. Si le trafic réseau d'une instance de serveur virtuel commence à avoir un impact négatif significatif sur d'autres serveurs virtuels, cette instance peut être redémarrée sur un nouvel hôte ou, dans des cas extrêmes, complètement désactivée. Cet impact négatif est souvent observé lorsque les niveaux de trafic approchent les 20 000 à 30 000 paquets par seconde (PPS).  Pour une mise en réseau garantie, l'utilisation de l'offre Serveur Virtuel Dédié est recommandée. Pour plus d'informations, voir l'offre [Serveur virtuel dédié](/docs/vsi?topic=virtual-servers-dedicated-virtual-servers) pour les environnements à service exclusif.

Les instances publiques se trouvent sur un hyperviseur partagé avec d'autres clients. Toutefois, les processeurs et la mémoire sont dédiés au serveur virtuel, ce qui rend les performances du serveur plus fiables.

Les serveurs virtuels suivants sont disponibles.

| Serveurs virtuels publics  | Description                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- |
| [Balanced](/docs/vsi?topic=virtual-servers-balanced#balanced) | Choix recommandé pour les charges de travail de cloud communes nécessitant un équilibre entre les performances et l'évolutivité. Utilise un stockage sur réseau.|
| [Stockage Balanced Local](/docs/vsi?topic=virtual-servers-balanced-local-storage#balanced-local-storage) | Choix recommandé pour les clusters de base de données de grande taille exigeant des performances d'E-S élevées à faible temps d'attente.|
| [Compute](/docs/vsi?topic=virtual-servers-compute#compute) | Choix recommandé pour les charges de travail de trafic Web modéré à élevé.|
| [Memory](/docs/vsi?topic=virtual-servers-memory#memory)  | Choix recommandé pour les charges de travail d'analyse en temps réel et de mise en cache de mémoire. |
| [GPU](/docs/vsi?topic=virtual-servers-gpu#gpu)  | Choix optimal pour les charges de travail à performances élevées.
{: caption="Tableau 1. Serveurs virtuels publics pris en charge" caption-side="top"}

Certaines de ces familles sont également disponibles pour IBM Cloud Virtual Servers for VPC. Pour plus d'informations, voir [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen).
{:tip}

## Etapes suivantes

Une fois que vous avez défini la version de votre serveur virtuel, mettez à disposition votre serveur public virtuel. Pour commencer, consultez les rubriques suivantes :
1. [Mise à disposition de sélections](/docs/vsi?topic=virtual-servers-provisioning-selections)
2. [Mise à disposition d'instances publiques](/docs/vsi?topic=virtual-servers-ordering-vs-public)
