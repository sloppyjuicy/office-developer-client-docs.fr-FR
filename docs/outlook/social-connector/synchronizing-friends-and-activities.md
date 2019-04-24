---
title: Synchronisation des amis et des activités
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: Outlook Social Connector (OSC) prend en charge l'affichage d'informations à partir d'un réseau social sur une personne figurant dans la carte de visite ou dans le volet de contacts Outlook. SharePoint Server, SharePoint Workspace, le client Lync et toutes les applications clientes Office qui prennent en charge les informations de présence prennent en charge la carte de visite.
ms.openlocfilehash: 0d6881c5d596519422d01ca61a00b1a68e610f2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329200"
---
# <a name="synchronizing-friends-and-activities"></a>Synchronisation des amis et des activités

Outlook Social Connector (OSC) prend en charge l'affichage d'informations à partir d'un réseau social sur une personne figurant dans la carte de visite ou dans le volet de contacts Outlook. SharePoint Server, SharePoint Workspace, le client Lync et toutes les applications clientes Office qui prennent en charge les informations de présence prennent en charge la carte de visite.
  
Vous pouvez utiliser la carte de visite dans les scénarios de collaboration dans les applications Office pour en savoir plus sur les personnes avec lesquelles vous collaborez. Les exemples de ces scénarios incluent la messagerie dans Outlook et la co-création d'un document dans Word. Lorsque vous cliquez sur l'onglet **Nouveautés** d'une carte de visite, le affiche des informations sur cette personne. 
  
Le volet de contacts Outlook affiche des informations sur une personne qui peut être l'expéditeur ou le destinataire d'un élément Outlook que vous avez sélectionné. Lorsque vous sélectionnez une autre personne dans le volet contacts ou un autre élément de l'explorateur Outlook, ou si vous ouvrez un élément Outlook dans un inspecteur, Outlook Social Connector (OSC) actualise le volet personnes. 
  
Pour que la carte de visite ou le volet personnes affiche les informations actuelles de la personne sélectionnée, le OSC synchronise ces informations par le biais des fournisseurs OSC et d'une mise en cache. Cette synchronisation dépend des fournisseurs OSC installés sur l'ordinateur client, des réseaux sociaux sur lesquels vous avez ouvert une session via leurs fournisseurs OSC et du mode de synchronisation pris en charge par chacun des fournisseurs OSC.
  
Le OSC prend en charge la synchronisation des amis, des amis et des activités pour les amis et les non Friends de différentes façons: la synchronisation mise en cache, la synchronisation à la demande et la synchronisation hybride. La principale différence entre ces modes de synchronisation est l'emplacement où OSC stocke les données, qu'il s'agisse d'un dossier dans la Banque Outlook par défaut de l'utilisateur ou de la mémoire sur l'ordinateur de l'utilisateur. Dans chaque cas, comme indiqué dans cette rubrique, il existe une durée minimale par défaut pendant laquelle les données demeurent dans le dossier ou la mémoire avant l'actualisation des données. Dans certains cas, la durée minimale peut être personnalisée par la stratégie de groupe. Pour plus d'informations sur les stratégies de groupe qui contrôlent le comportement du OSC, voir [Comment gérer Outlook Social Connector à l'aide](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)de la stratégie de groupe.
  
Notez que si la personne sélectionnée n'est pas membre du réseau social, le OSC n'affiche pas d'informations sur la personne ou l'activité de cette personne dans la carte de visite ou dans le volet des personnes.
  
## <a name="cached-synchronization"></a>Synchronisation mise en cache

Un fournisseur OSC peut stocker des informations pour les amis sur le réseau social dans un dossier spécifique sur le magasin Outlook par défaut de l'utilisateur et mettre à jour régulièrement ce cache une fois qu'une durée spécifiée a expiré. La mise en cache des informations dans un dossier présente l'avantage de réduire le trafic vers le réseau social.
  
> [!NOTE]
> À partir d'Outlook Social Connector 2013, le OSC ne prend plus en charge la synchronisation mise en cache des activités. 
  
### <a name="cached-synchronization-of-friends"></a>Synchronisation des amis mise en cache

Si un fournisseur OSC prend en charge la synchronisation mise en cache pour les amis, le OSC met en cache les informations des amis de l'utilisateur connecté sur le réseau social. Les informations sont mises en cache dans un dossier de contacts Outlook qui est propre à ce réseau social dans la Banque Outlook par défaut de l'utilisateur. Le nom du dossier contacts est basé sur le nom du réseau social, que l'OSC obtient à l'aide de la propriété [ISocialProvider:: SocialNetworkName](isocialprovider-socialnetworkname.md) . 
  
Dans la synchronisation mise en cache, OSC stocke les informations des amis de l'utilisateur connecté uniquement sur le réseau social. Le OSC n'accède pas aux informations pour les non-Friends.
  
L'intervalle par défaut de l'option OSC pour actualiser le dossier de contacts pour les informations des amis à partir du réseau social est une fois par jour (ou une fois par 1440 minutes). Cet intervalle d'actualisation peut également être défini par la stratégie de groupe, comme indiqué au début de cette rubrique.
  
Si une erreur se produit lors d'une actualisation, l'objet OSC effectue une nouvelle tentative à un intervalle spécifié par l'élément **contactSyncRestartInterval** dans le code XML **Capabilities** . Cette nouvelle tentative a une valeur par défaut de 30 minutes et peut également être définie par la stratégie de groupe. 
  
Lorsqu'un utilisateur ouvre une carte de visite et clique sur l'onglet **what's New** , l'onglet **what's New est** actualisé. De même, lorsqu'un utilisateur d'Outlook sélectionne un élément dans Outlook ou resélectionne une personne dans le volet personnes, le volet personnes est actualisé. Si l'intervalle d'actualisation du cache n'a pas expiré, le OSC accède au cache pour obtenir des informations sur l'utilisateur sélectionné. Cela évite l'utilisation de l'extensibilité du fournisseur OSC pour accéder au réseau social. Si l'intervalle d'actualisation a expiré, le OSC appelle la méthode [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) pour obtenir les informations des amis actuelles de l'utilisateur connecté et met à jour le cache dans le dossier contacts. 
  
Le fournisseur OSC informe OSC qu'il prend en charge la synchronisation mise en cache des amis en spécifiant les éléments suivants dans les **fonctionnalités** XML: 
  
- **getFriends** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **false**
    
## <a name="on-demand-synchronization"></a>Synchronisation à la demande

Lorsqu'un utilisateur clique sur l'onglet **what's New** dans une carte de visite, ou sélectionne un autre élément Outlook ou une autre personne dans le volet de personnes dans Outlook, le OSC actualise respectivement le volet de la carte de visite ou des personnes. Si un fournisseur OSC prend en charge la synchronisation à la demande de personnes ou d'activités, le OSC se synchronise avec un cache en mémoire et met à jour les détails, tels que le nom, le titre, l'image et les flux d'activité, sur la carte de visite ou le volet des personnes. Pour la synchronisation à la demande, contrairement à la synchronisation mise en cache, OSC tente d'actualiser les informations de la personne, que cette personne soit un ami ou non Friend de l'utilisateur connecté sur le réseau social. 
  
Les données de personne à la demande (ou activité) sont stockées en mémoire uniquement. Les données en mémoire sont effacées lorsque l'application cliente Office s'arrête, ou l'utilisateur provoque une actualisation de la carte de visite ou du volet personnes et les données sont restées en mémoire pendant plus longtemps que l'intervalle d'actualisation. Notez que l'actualisation à partir du réseau social est toujours lancée par un utilisateur actualisant la carte de visite ou le volet personnes (par exemple, en sélectionnant un autre utilisateur dans le volet personnes ou en sélectionnant un autre élément dans la fenêtre de l'explorateur Outlook). 

Toutefois, l'inverse n'est pas toujours true (toutes les actualisations de la carte de visite ou du volet des personnes n'entraînent pas nécessairement une actualisation à partir du réseau social). Si l'utilisateur actualise la carte de visite ou le volet de personnes, et que les données de personne (ou d'activité) sont restées en mémoire pendant plus longtemps que l'intervalle d'actualisation, le OSC appelle [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md) (ou [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md)) pour Mettez à jour les informations en mémoire à partir du réseau social. La période autorisée pour les informations Friend et non Friend en mémoire est de 24 heures, et pour les activités, 30 minutes. 
  
Une différence importante entre la synchronisation à la demande et la mise en cache est que la synchronisation à la demande peut extraire des informations de personne et d'activité pour des amis et des non-Friends sur le réseau. Si la personne sélectionnée n'est pas un ami, le OSC actualise les informations et les activités de cette personne si l'une des conditions suivantes est remplie: 
  
- La personne est un utilisateur du réseau social et permet la consultation publique des informations de profil et d'activité.
    
- La personne se trouve sur le même réseau que l'utilisateur connecté sur ce réseau social (par exemple, dans le même réseau pour l'Université Alumni).
    
La synchronisation à la demande de personnes et d'activités entraîne un plus grand nombre d'appels au fournisseur à partir du moteur de base OSC. Les réseaux sociaux doivent être en mesure de prendre en charge les besoins accrus de bande passante de la synchronisation à la demande.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Spécification des éléments XML pour la synchronisation à la demande

Le fournisseur OSC informe OSC qu'il prend en charge la synchronisation à la demande des amis et des non-amis en spécifiant les éléments suivants dans les **fonctionnalités** XML: 
  
- **getFriends** = **true**
    
- **cacheFriends** = **false**
    
- **dynamicContactsLookup** = **true**
    
Le fournisseur OSC informe OSC qu'il prend en charge la synchronisation à la demande des activités en spécifiant les éléments suivants dans les **fonctionnalités** XML: 
  
- **GetActivities** = **true**
    
- **cacheActivities** = **false**
    
- **dynamicActivitiesLookupEx** = **true**
    
## <a name="hybrid-synchronization"></a>Synchronisation hybride

Un fournisseur OSC peut prendre en charge la synchronisation hybride d'amis et de non-amis. Cela permet d'optimiser les appels entre le moteur de base OSC et le fournisseur OSC, les appels vers le réseau social pour la synchronisation à la demande des amis et la devise des données des amis. La durée minimale pendant laquelle les données peuvent rester dans un dossier ou une mémoire, le cas échéant, sont identiques à celles des modes de synchronisation à la demande ou mis en cache.
  
> [!NOTE]
> À partir d'Outlook Social Connector 2013, le OSC prend en charge uniquement la synchronisation à la demande des activités et ne prend plus en charge la synchronisation hybride des activités. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Synchronisation hybride d'amis et de non-amis

Si un fournisseur OSC prend en charge la synchronisation hybride des amis et des non-amis, le OSC effectue les opérations suivantes: 
  
- OSC stocke des informations pour les amis de l'utilisateur connecté dans le dossier de contacts spécifique au réseau social.
    
- OSC stocke des informations pour les non-amis de l'utilisateur connecté en mémoire.
    
Le fournisseur OSC informe OSC qu'il prend en charge la synchronisation hybride des amis et des non-amis en spécifiant les éléments suivants dans les **fonctionnalités** XML: 
  
- **getFriends** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **true**
    
## <a name="synchronization-intervals"></a>Intervalles de synchronisation

Le tableau suivant récapitule les intervalles de synchronisation pour les informations des amis et des non-amis entre le cache correspondant (dossier ou mémoire) et le réseau social, en fonction du mode de synchronisation pris en charge. Pour le mode de synchronisation hybride, reportez-vous aux lignes correspondant au mode mis en cache pour les amis et à la ligne du mode à la demande pour les non-amis.
  
|**Mode de synchronisation pour les personnes**|**Où l'intervalle d'actualisation est défini**|**Durée minimale par défaut avant actualisation**|**Remplacement de la stratégie de groupe**|
|:-----|:-----|:-----|:-----|
|Mise en cache  <br/> |Défini dans OSC  <br/> |1440 minutes (24 heures)  <br/> |Valeur de Registre Windows **NetContactSyncInterval** <br/> |
|Mise en cache  <br/> |élément **contactSyncRestartInterval** dans les **fonctionnalités** XML  <br/> |30 minutes si **contactSyncRestartInterval** n'est pas défini  <br/> |Valeur de Registre Windows **contactSyncRestartInterval** <br/> |
|À la demande  <br/> |Défini dans OSC  <br/> |1440 minutes (24 heures)  <br/> |Valeur de Registre Windows **OnlineSearchExpiryTime** <br/> |
   
Le tableau suivant récapitule les intervalles de synchronisation pour les activités des amis et des non-amis entre le cache correspondant (dossier ou mémoire) et le réseau social, en fonction des modes de synchronisation pris en charge. 
  
|**Mode de synchronisation pour les activités**|**Où l'intervalle d'actualisation est défini**|**Durée minimale par défaut avant actualisation**|**Remplacement de la stratégie de groupe**|
|:-----|:-----|:-----|:-----|
|À la demande  <br/> |Défini dans OSC  <br/> |30 minutes  <br/> |Valeur de Registre Windows **OnlineSearchExpiryTime** <br/> |
   
Les informations suivantes s'appliquent aux valeurs du Registre Windows indiquées dans les deux tableaux:
  
- Flèche`HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Valeur: valeur DWORD comprise entre 1 et 10080
    
## <a name="see-also"></a>Voir aussi

- [Exemple de XML de fonctionnalités](capabilities-xml-example.md)  
- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Comment gérer Outlook Social Connector à l'aide de la stratégie de groupe](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

