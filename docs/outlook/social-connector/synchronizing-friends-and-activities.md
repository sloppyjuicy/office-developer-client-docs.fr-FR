---
title: Synchronisation des amis et des activités
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: Le Outlook Social Connector (OSC) prend en charge l’affichage d’informations à partir d’un réseau social sur une personne dans la carte de visite ou dans le Outlook contacts. SharePoint Le serveur, SharePoint workspace, le client Lync et toutes les applications clientes Office prise en charge des informations de présence la prise en charge de la carte de visite.
ms.openlocfilehash: 0d6881c5d596519422d01ca61a00b1a68e610f2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329200"
---
# <a name="synchronizing-friends-and-activities"></a>Synchronisation des amis et des activités

Le Outlook Social Connector (OSC) prend en charge l’affichage d’informations à partir d’un réseau social sur une personne dans la carte de visite ou dans le Outlook contacts. SharePoint Le serveur, SharePoint workspace, le client Lync et toutes les applications clientes Office prise en charge des informations de présence la prise en charge de la carte de visite.
  
Vous pouvez utiliser la carte de visite dans des scénarios de collaboration Office applications pour en savoir plus sur les personnes avec qui vous collaborez. Voici quelques exemples de ces scénarios : la messagerie Outlook et la co-auteur d’un document dans Word. Lorsque vous cliquez sur l’onglet Nouveautés **d’une** carte de visite, les informations sur cette personne s’affichent. 
  
Le Outlook De personnes affiche des informations sur une personne qui peut être un expéditeur ou un destinataire d’un Outlook que vous avez sélectionné. Chaque fois que vous sélectionnez une autre personne dans le volet Personnes ou un autre élément dans l’explorateur Outlook, ou que vous ouvrez un élément Outlook dans un inspecteur, Outlook Social Connector (OSC) actualisera le volet Personnes. 
  
Pour que la carte de visite ou le volet Contacts affiche les informations actuelles de la personne sélectionnée, l’OSC synchronise ces informations par le biais des fournisseurs OSC et d’une forme de mise en cache. Cette synchronisation dépend des fournisseurs OSC installés sur l’ordinateur client, des réseaux sociaux que vous avez connectés via leurs fournisseurs OSC et du mode de synchronisation que chacun des fournisseurs OSC pour ces réseaux sociaux prend en charge.
  
L’OSC prend en charge la synchronisation des amis, des non-amis et des activités pour les amis et les non-amis de différentes manières : synchronisation mise en cache, synchronisation à la demande et synchronisation hybride. La principale différence entre ces modes de synchronisation est l’endroit où OSC stocke les données, qu’il s’agit d’un dossier du magasin Outlook par défaut de l’utilisateur ou de la mémoire sur l’ordinateur de l’utilisateur. Dans chaque cas, comme indiqué dans cette rubrique, il existe une durée minimale par défaut pendant qui reste les données dans le dossier ou la mémoire avant l’actualisation des données. Dans certains cas, la durée minimale peut être personnalisée par la stratégie de groupe. Pour plus d’informations sur les stratégies de groupe qui contrôlent le comportement de l’OSC, voir Comment gérer le connecteur social Outlook à l’aide de [la stratégie de groupe](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103).
  
Notez que si la personne sélectionnée n’est pas membre du réseau social, l’OSC n’affiche aucune information sur la personne ou l’activité de cette personne dans la carte de visite ou le volet Contacts.
  
## <a name="cached-synchronization"></a>Synchronisation mise en cache

Un fournisseur OSC peut stocker des informations pour des amis sur le réseau social dans un dossier spécifique du magasin d’Outlook par défaut de l’utilisateur et mettre régulièrement à jour ce cache après expiration d’une durée spécifiée. La mise en cache des informations dans un dossier présente l’avantage de réduire le trafic vers le réseau social.
  
> [!NOTE]
> À compter Outlook Social Connector 2013, OSC ne prend plus en charge la synchronisation des activités mises en cache. 
  
### <a name="cached-synchronization-of-friends"></a>Synchronisation mise en cache des amis

Si un fournisseur OSC prend en charge la synchronisation mise en cache pour les amis, l’OSC met en cache les informations des amis de l’utilisateur connecté sur le réseau social. Les informations sont mises en cache dans un dossier Outlook contacts spécifiques à ce réseau social dans le magasin d’Outlook par défaut de l’utilisateur. Le nom du dossier contacts est basé sur le nom du réseau social, que l’OSC obtient à l’aide de la propriété [ISocialProvider::SocialNetworkName.](isocialprovider-socialnetworkname.md) 
  
Dans la synchronisation mise en cache, OSC stocke uniquement les informations des amis de l’utilisateur connecté sur le réseau social. L’OSC n’accède pas aux informations des non-amis.
  
L’intervalle par défaut pour qu’OSC actualise le dossier de contacts pour les informations des amis à partir du réseau social est une fois par jour (ou une fois par 1 440 minutes). Cet intervalle d’actualisation peut également être définie par la stratégie de groupe, comme expliqué au début de cette rubrique.
  
Si une erreur se produit lors d’une actualisation, l’OSC retente à un intervalle spécifié par l’élément **contactSyncRestartInterval** dans le **XML** des fonctionnalités. Cet intervalle de nouvelle tentative a une valeur par défaut de 30 minutes et peut également être définie par la stratégie de groupe. 
  
Lorsqu’un utilisateur ouvre une carte de visite et sélectionne **l’onglet** Nouveautés, **l’onglet** Nouveautés est actualisé. De même, lorsqu’un Outlook resélectionne un élément dans Outlook ou réélectionne une personne dans le volet Personnes, le volet Personnes est actualisé. Si l’intervalle d’actualisation du cache n’a pas expiré, l’OSC se rend dans le cache pour obtenir des informations pour l’utilisateur sélectionné. Cela permet d’éviter la surcharge de l’utilisation de l’extensibilité du fournisseur OSC pour accéder au réseau social. Si l’intervalle d’actualisation a expiré, l’OSC appelle la méthode [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) pour obtenir les informations des amis actuels de l’utilisateur connecté et met à jour le cache dans le dossier contacts. 
  
Le fournisseur OSC informe l’OSC qu’il prend en charge la synchronisation mise en cache des amis en spécifiant les éléments suivants dans le XML **des fonctionnalités** : 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **true**
    
- **dynamicContactsLookup**  =  **false**
    
## <a name="on-demand-synchronization"></a>Synchronisation à la demande

Lorsqu’un utilisateur sélectionne l’onglet Nouveautés **d’une** carte de visite ou sélectionne un autre élément Outlook ou une autre personne dans le volet Contacts de Outlook, l’OSC actualisera respectivement la carte de visite ou le volet Contacts. Si un fournisseur OSC prend en charge la synchronisation à la demande des personnes ou des activités, l’OSC se synchronise avec un cache en mémoire et met à jour les détails, tels que le nom, le titre, l’image et les flux d’activités, sur la carte de visite ou le volet Contacts. Pour la synchronisation à la demande, contrairement à la synchronisation mise en cache, l’OSC tente d’actualiser les informations de la personne, qu’elle soit un ami ou non de l’utilisateur connecté sur le réseau social. 
  
Les données de personne (ou d’activité) à la demande sont stockées en mémoire uniquement. Les données en mémoire sont effacées lorsque l’application cliente Office s’arrête, ou l’utilisateur entraîne une actualisation de la carte de visite ou du volet Contacts et les données sont restés en mémoire pendant une durée plus longue que l’intervalle d’actualisation. Notez que l’actualisation du réseau social est toujours initiée par un utilisateur actualisé la carte de visite ou le volet Contacts (par exemple, en sélectionnant un autre utilisateur dans le volet Contacts ou en sélectionnant un autre élément dans la fenêtre d’explorateur Outlook). 

Toutefois, l’inverse n’est pas toujours vrai : chaque actualisation de la carte de visite ou du volet Contacts n’entraîne pas nécessairement une actualisation à partir du réseau social. Si l’utilisateur actualisation la carte de visite ou le volet Contacts et que les données de la personne (ou de l’activité) sont restés en mémoire pendant une durée plus longue que l’intervalle d’actualisation, l’OSC appelle [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) (ou [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)) pour mettre à jour les informations en mémoire à partir du réseau social. La période autorisée pour les informations d’amis et de non-amis en mémoire est de 24 heures et pour les activités, de 30 minutes. 
  
Une différence importante entre la synchronisation mise en cache et la synchronisation à la demande est que la synchronisation à la demande peut récupérer des informations sur la personne et l’activité pour des amis et des non-amis sur le réseau. Si la personne sélectionnée n’est pas un ami, l’OSC actualne les informations et les activités de cette personne si l’une des conditions suivantes est remplie : 
  
- La personne est un utilisateur sur le réseau social et permet l’affichage public des informations de profil et d’activité.
    
- La personne se trouve sur le même réseau que l’utilisateur connecté sur ce réseau social (par exemple, dans le même réseau pour les anciens élèves de l’université).
    
La synchronisation à la demande des personnes et des activités entraîne davantage d’appels au fournisseur à partir du moteur principal OSC. Les réseaux sociaux doivent être en mesure de gérer les besoins accrus en bande passante de la synchronisation à la demande.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Spécification d’éléments XML pour la synchronisation à la demande

Le fournisseur OSC informe l’OSC qu’il prend en charge la synchronisation à la demande des amis et des non-amis en spécifiant les éléments suivants dans le **XML** des fonctionnalités : 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **false**
    
- **dynamicContactsLookup**  =  **true**
    
Le fournisseur OSC informe l’OSC qu’il prend en charge la synchronisation à la demande des activités en spécifiant les éléments suivants dans les fonctionnalités **XML** : 
  
- **getActivities**  =  **true**
    
- **cacheActivities**  =  **false**
    
- **dynamicActivitiesLookupEx**  =  **true**
    
## <a name="hybrid-synchronization"></a>Synchronisation hybride

Un fournisseur OSC peut prendre en charge la synchronisation hybride des amis et des non-amis. Cela permet d’optimiser les appels entre le moteur principal OSC et le fournisseur OSC, les appels au réseau social pour la synchronisation à la demande des amis et la devise des données des amis. La durée minimale pendant laquelle les données peuvent rester dans un dossier ou une mémoire, le cas échéant, est identique aux limites des modes de synchronisation mis en cache ou à la demande.
  
> [!NOTE]
> À compter Outlook Social Connector 2013, OSC prend en charge uniquement la synchronisation à la demande des activités et ne prend plus en charge la synchronisation hybride des activités. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Synchronisation hybride des amis et des non-amis

Si un fournisseur OSC prend en charge la synchronisation hybride d’amis et de non-amis, l’OSC fait les choses suivantes : 
  
- OsC stocke les informations des amis de l’utilisateur connecté dans le dossier de contacts spécifique au réseau social.
    
- L’OSC stocke des informations pour les non-amis de l’utilisateur connecté en mémoire.
    
Le fournisseur OSC informe l’OSC qu’il prend en charge la synchronisation hybride des amis et des non-amis en spécifiant les éléments suivants dans le XML **des fonctionnalités** : 
  
- **getFriends**  =  **true**
    
- **cacheFriends**  =  **true**
    
- **dynamicContactsLookup**  =  **true**
    
## <a name="synchronization-intervals"></a>Intervalles de synchronisation

Le tableau suivant récapitule les intervalles de synchronisation pour les informations d’amis et de non-amis entre le cache correspondant (dossier ou mémoire) et le réseau social, en fonction du mode de synchronisation pris en charge. Pour le mode de synchronisation hybride, reportez-vous aux lignes pour le mode mis en cache pour les amis et à la ligne pour le mode à la demande pour les non-amis.
  
|**Mode de synchronisation pour les personnes**|**Où l’intervalle d’actualisation est définie**|**Durée minimale par défaut avant l’actualisation**|**Remplacement de stratégie de groupe**|
|:-----|:-----|:-----|:-----|
|Mise en cache  <br/> |Définir dans OSC  <br/> |1 440 minutes (24 heures)  <br/> |Windows de Registre **NetContactSyncInterval** <br/> |
|Mise en cache  <br/> |**élément contactSyncRestartInterval dans** **les fonctionnalités** XML  <br/> |30 minutes si **contactSyncRestartInterval n’est** pas définie  <br/> |Windows de registre **contactSyncRestartInterval** <br/> |
|À la demande  <br/> |Définir dans OSC  <br/> |1 440 minutes (24 heures)  <br/> |Windows de Registre **OnlineSearchExpiryTime** <br/> |
   
Le tableau suivant récapitule les intervalles de synchronisation pour les activités des amis et des non-amis entre le cache correspondant (dossier ou mémoire) et le réseau social, en fonction des modes de synchronisation pris en charge. 
  
|**Mode de synchronisation des activités**|**Où l’intervalle d’actualisation est définie**|**Durée minimale par défaut avant l’actualisation**|**Remplacement de stratégie de groupe**|
|:-----|:-----|:-----|:-----|
|À la demande  <br/> |Définir dans OSC  <br/> |30 minutes  <br/> |Windows de Registre **OnlineSearchExpiryTime** <br/> |
   
Les informations suivantes s’appliquent aux Windows de Registre répertoriées dans les deux tableaux :
  
- Clé :  `HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- Valeur : valeur DWORD entre 1 et 10080
    
## <a name="see-also"></a>Voir aussi

- [Exemple de fonctionnalités XML](capabilities-xml-example.md)  
- [XML pour les fonctionnalités](xml-for-capabilities.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Comment gérer le connecteur social Outlook à l’aide de la stratégie de groupe](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

