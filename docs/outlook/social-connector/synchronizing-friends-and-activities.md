---
title: Synchronisation des amis et des activités
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6e91b765-a207-4d8c-8763-5d643ca4d0c0
description: L’Outlook Social Connector (OSC) prend en charge l’affichage des informations à partir d’un réseau social sur une personne dans la carte de visite ou dans le volet personnes Outlook. SharePoint Server, SharePoint Workspace, client Lync et toutes les applications clientes Office qui prennent en charge les informations de présence prend en charge la carte de visite.
ms.openlocfilehash: 0d6881c5d596519422d01ca61a00b1a68e610f2c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399157"
---
# <a name="synchronizing-friends-and-activities"></a>Synchronisation des amis et des activités

L’Outlook Social Connector (OSC) prend en charge l’affichage des informations à partir d’un réseau social sur une personne dans la carte de visite ou dans le volet personnes Outlook. SharePoint Server, SharePoint Workspace, client Lync et toutes les applications clientes Office qui prennent en charge les informations de présence prend en charge la carte de visite.
  
Vous pouvez utiliser la carte de visite dans les scénarios de collaboration dans les applications Office pour en savoir plus sur les personnes avec qu'auquel vous collaborez. Les exemples de ces scénarios de messagerie dans Outlook et la co-création d’un document dans Word. Lorsque vous cliquez sur l’onglet **Quelles sont les nouveautés** d’une carte de visite, affiche des informations relatives à cette personne. 
  
Le volet personnes Outlook affiche des informations sur une personne qui peut être un expéditeur ou un destinataire d’un élément Outlook que vous avez sélectionné. Lorsque vous sélectionnez une autre personne dans le volet personnes ou un autre élément dans l’Explorateur Outlook, ou ouvrez un élément Outlook dans un inspecteur, l’Outlook Social Connector (OSC) actualise le volet personnes. 
  
Pour la carte de visite ou le volet personnes afficher les informations en cours de la personne sélectionnée, le OSC synchronise ces informations via les fournisseurs OSC et qu’une forme de mise en cache. Cette synchronisation varie selon les fournisseurs OSC qui sont installés sur l’ordinateur client, que vous avez connecté grâce à leurs fournisseurs OSC et le mode de synchronisation que chacun des fournisseurs OSC social ces réseaux prend en charge les réseaux sociaux.
  
L’OSC prend en charge amis, non amis et des activités de synchronisation pour vos amis et non amis de différentes manières : mis en cache de la synchronisation, la synchronisation de la demande et la synchronisation hybride. La différence principale entre ces modes de synchronisation est où l’OSC stocke les données, s’il s’agit d’un dossier dans le magasin d’Outlook par défaut de l’utilisateur, ou dans la mémoire sur l’ordinateur de l’utilisateur. Dans chaque cas comme indiqué précédemment dans cette rubrique, il existe une durée minimale par défaut que les données demeurent dans la mémoire ou le dossier avant l’actualisation des données. Dans certains cas, la quantité minimale de temps peut être personnalisée par la stratégie de groupe. Pour plus d’informations sur les stratégies de groupe qui contrôlent le comportement de l’OSC, voir [comment gérer Outlook Social Connector à l’aide de la stratégie de groupe](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103).
  
Notez que si la personne sélectionnée n’est pas un membre du réseau social, l’OSC n’affiche aucune information personne ou une activité pour cette personne dans la carte de visite ou le volet personnes.
  
## <a name="cached-synchronization"></a>Synchronisation mis en cache

Un fournisseur OSC peut stocker des informations pour vos amis sur le réseau social dans un dossier spécifique sur le magasin d’Outlook par défaut de l’utilisateur et mettre régulièrement à jour ce cache après qu’un laps de temps spécifié a expiré. La mise en cache des informations dans un dossier a l’avantage de réduire le trafic vers le réseaux sociaux.
  
> [!NOTE]
> Démarrage d’Outlook Social Connector 2013, l’OSC ne gère plus mis en cache de synchronisation des activités. 
  
### <a name="cached-synchronization-of-friends"></a>Synchronisation de mise en cache d’amis

Si un fournisseur OSC prend en charge la mise en cache de la synchronisation pour vos amis, le OSC met en cache pour vos amis de l’utilisateur connecté sur le réseau social. Les informations sont mis en cache dans un dossier de contacts Outlook qui est spécifique à ce réseau social dans le magasin d’Outlook par défaut de l’utilisateur. Le nom du dossier contacts est basé sur le nom de réseau social, qui le OSC obtienne à l’aide de la propriété [ISocialProvider::SocialNetworkName](isocialprovider-socialnetworkname.md) . 
  
Synchronisation mis en cache, de l’OSC stocke des informations pour seulement vos amis connecté l’utilisateur sur le réseau social. Informations pour non amis n’ont pas accès l’OSC.
  
L’intervalle par défaut pour l’OSC actualiser le dossier contacts pour les informations de vos amis à partir du réseau social est une fois par jour (ou une fois par 1 440 minutes). Cet intervalle d’actualisation peut également être définie par la stratégie de groupe, comme indiqué au début de cette rubrique.
  
Si une erreur se produit au cours d’une actualisation, l’OSC réessayer à un intervalle spécifié par l’élément **contactSyncRestartInterval** dans le XML des **fonctionnalités** . Cet intervalle entre tentatives a une valeur par défaut de 30 minutes et peut également être défini par la stratégie de groupe. 
  
Lorsqu’un utilisateur ouvre une carte de visite et sélectionne l’onglet **Quelles sont les nouveautés** , l’onglet **Nouveautés** actualise. De même, lorsqu’un utilisateur Outlook sélectionne un élément dans Outlook à nouveau ou sélectionne à nouveau une personne dans le volet personnes, le volet personnes est actualisée. Si l’intervalle d’actualisation du cache n’a pas expiré, l’OSC accède au cache pour obtenir des informations de l’utilisateur sélectionné. Cela évite d’accéder au réseau social à l’aide de l’extensibilité de fournisseur OSC. Si l’intervalle d’actualisation a expiré, l’OSC appelle la méthode [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) pour obtenir des informations de vos amis en cours de l’utilisateur connecté et met à jour le cache dans le dossier contacts. 
  
Le fournisseur OSC informe l’OSC qu’il prend en charge synchronisation mise en cache d’amis en spécifiant les éléments suivants dans le XML des **fonctionnalités** : 
  
- **getFriends** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **false**
    
## <a name="on-demand-synchronization"></a>Synchronisation de la demande

Lorsqu’un utilisateur sélectionne l’onglet **Quelles sont les nouveautés** dans une carte de visite, ou un autre élément Outlook ou une autre personne dans le volet personnes dans Outlook, l’OSC actualise respectivement la carte de visite ou le volet personnes. Si un fournisseur OSC prend en charge la synchronisation à la demande des personnes ou des activités, l’OSC se synchronise avec un cache en mémoire et met à jour les détails, tels que le nom, titre, des images et flux d’activité, sur la carte de visite ou le volet personnes. Pour la synchronisation de la demande, contrairement à la synchronisation mis en cache, l’OSC tente d’actualiser les informations de la personne que cette personne soit un ami ou un autre ami de l’utilisateur connecté sur le réseau social. 
  
Données personne (ou une activité) de la demande sont stockées en mémoire uniquement. Les données en mémoire sont désactivées lors de l’application cliente Office s’arrête, ou l’utilisateur entraîne une actualisation de la carte de visite ou le volet personnes et les données sont resté en mémoire pendant plus de l’intervalle d’actualisation. Notez que l’actualisation à partir du réseau social est toujours initiée par un utilisateur de l’actualisation de la carte de visite ou le volet personnes, (par exemple, en sélectionnant un autre utilisateur dans le volet personnes, ou en sélectionnant un autre élément dans la fenêtre de l’Explorateur Outlook). 

Toutefois, l’inverse n’est pas toujours true, non à chaque actualisation de la carte de visite ou le volet personnes implique nécessairement une actualisation à partir du réseau social. Si l’utilisateur actualise la carte de visite ou données volet personnes et la personne (ou une activité) sont resté en mémoire pendant plus de l’intervalle d’actualisation, l’OSC appelle [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) (ou [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md)) à mettre à jour les informations en mémoire à partir du réseau social. La période autorisée pour plus d’informations ami et non ami en mémoire est de 24 heures et activités, 30 minutes. 
  
Une des différences importantes entre synchronisation mis en cache et la demande sont que la synchronisation de la demande peut extraire les informations d’activité et de la personne d’amis et non amis sur le réseau. Si la personne sélectionnée est un ami-non, l’OSC actualise les informations et les activités correspondant à cette personne si une des conditions suivantes est remplie : 
  
- La personne est un utilisateur sur le réseau social et permet l’affichage public des informations de profil et son activité.
    
- La personne est dans le même réseau que l’utilisateur connecté sur ce réseau social (par exemple, dans le même réseau anciens élèves université).
    
Synchronisation de la demande des personnes et des activités génère plus d’appels au fournisseur à partir du moteur de base OSC. Les réseaux sociaux doivent être en mesure de gérer la bande passante accrue de la synchronisation de la demande.
  
### <a name="specifying-xml-elements-for-on-demand-synchronization"></a>Spécification des éléments XML pour la synchronisation de la demande

Le fournisseur OSC informe l’OSC qu’elle prend en charge la synchronisation de la demande d’amis et non amis en spécifiant les éléments suivants dans le XML des **fonctionnalités** : 
  
- **getFriends** = **true**
    
- **cacheFriends** = **false**
    
- **dynamicContactsLookup** = **true**
    
Le fournisseur OSC informe l’OSC qu’il prend en charge à la demande sur la synchronisation des activités en spécifiant les éléments suivants dans le XML des **fonctionnalités** : 
  
- **getActivities** = **true**
    
- **cacheActivities** = **false**
    
- **dynamicActivitiesLookupEx** = **true**
    
## <a name="hybrid-synchronization"></a>Synchronisation hybride

Un fournisseur OSC peut prendre en charge la synchronisation hybride des amis et non amis. Cela permet d’optimiser les appels entre le moteur de base OSC et le fournisseur OSC, les appels au réseau social pour la synchronisation de la demande de vos amis et la devise de données des amis. La durée minimale que les données peuvent rester dans un dossier ou de la mémoire, le cas échéant, est la même que les limites dans les modes de synchronisation mis en cache ou à la demande.
  
> [!NOTE]
> Démarrage dans Outlook Social Connector 2013, l’OSC prend en charge uniquement la demande synchronisation des activités et ne prend en charge la synchronisation hybride d’activités. 
  
### <a name="hybrid-synchronization-of-friends-and-non-friends"></a>Synchronisation hybride des amis et non amis

Si un fournisseur OSC prend en charge la synchronisation hybride des amis et non amis, l’OSC effectue les opérations suivantes : 
  
- L’OSC stocke des informations pour vos amis de l’utilisateur connecté dans le dossier contact spécifiques du réseau social.
    
- L’OSC stocke des informations pour non amis de l’utilisateur connecté en mémoire.
    
Le fournisseur OSC informe l’OSC qu’elle prend en charge la synchronisation hybride d’amis et non amis en spécifiant les éléments suivants dans le XML des **fonctionnalités** : 
  
- **getFriends** = **true**
    
- **cacheFriends** = **true**
    
- **dynamicContactsLookup** = **true**
    
## <a name="synchronization-intervals"></a>Intervalles de synchronisation

Le tableau suivant récapitule les intervalles de synchronisation pour vos amis et informations non amis entre le cache correspondant (dossier ou la mémoire) et le réseaux sociaux, selon le mode de synchronisation pris en charge. Pour le mode de synchronisation hybride, consultez les lignes pour le mode mis en cache pour vos amis et la ligne pour le mode de la demande pour non amis.
  
|**Mode de synchronisation de personnes**|**Où intervalle d’actualisation est défini**|**Durée minimale par défaut avant l’actualisation**|**Remplacer la stratégie de groupe**|
|:-----|:-----|:-----|:-----|
|Mise en cache  <br/> |Définies dans OSC  <br/> |1440 minutes (24 heures)  <br/> |Valeur de Registre Windows **NetContactSyncInterval** <br/> |
|Mise en cache  <br/> |élément **contactSyncRestartInterval** de **fonctionnalités** XML  <br/> |30 minutes si **contactSyncRestartInterval** n’est pas définie.  <br/> |Valeur de Registre Windows **contactSyncRestartInterval** <br/> |
|À la demande  <br/> |Définies dans OSC  <br/> |1440 minutes (24 heures)  <br/> |Valeur de Registre Windows **OnlineSearchExpiryTime** <br/> |
   
Le tableau suivant récapitule les intervalles de la synchronisation des activités des amis et non amis entre le cache correspondant (dossier ou la mémoire) et le réseaux sociaux, selon les modes de synchronisation pris en charge. 
  
|**Mode de synchronisation pour les activités**|**Où intervalle d’actualisation est défini**|**Durée minimale par défaut avant l’actualisation**|**Remplacer la stratégie de groupe**|
|:-----|:-----|:-----|:-----|
|À la demande  <br/> |Définies dans OSC  <br/> |30 minutes  <br/> |Valeur de Registre Windows **OnlineSearchExpiryTime** <br/> |
   
Les informations suivantes s’applique aux valeurs de Registre Windows répertoriés dans les deux tables :
  
- Clé :`HKEY_CURRENT_USER\Software\Policies\Microsoft\Office\Outlook\SocialConnector`
    
- : Valeur valeur DWORD comprise entre 1 et 10080
    
## <a name="see-also"></a>Voir aussi

- [Exemple de code XML des fonctionnalités](capabilities-xml-example.md)  
- [Fichier XML pour les fonctionnalités](xml-for-capabilities.md)
- [Développement d'un fournisseur avec le schéma XML OSC](developing-a-provider-with-the-osc-xml-schema.md)  
- [Comment faire pour gérer Outlook Social Connector à l’aide de la stratégie de groupe](https://support.microsoft.com/default.aspx?scid=kb%3Ben-US%3B2020103)

