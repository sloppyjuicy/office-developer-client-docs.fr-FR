---
title: Objets du fournisseur de services MAPI
description: Décrit tous les objets du fournisseur de services MAPI, qui sont strictement destinés à la comptabilité; ils sont utilisés par MAPI pour contrôler les processus de démarrage et d’arrêt.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
ms.openlocfilehash: 34661acab74422b1b7d49acc14e675b44b4eb264
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828338"
---
# <a name="mapi-service-provider-objects"></a>Objets du fournisseur de services MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services implémentent de nombreux objets. Certaines sont principalement utilisées par MAPI et d’autres par des applications clientes. Quelques objets sont implémentés par tous les types de fournisseurs de services ; les autres sont spécifiques à un seul type de fournisseur. Le tableau suivant décrit tous les objets du fournisseur de services.
  
|**Objet fournisseur de services**|**Description**|
|:-----|:-----|
|Conteneur de carnet d’adresses  <br/> |Contient les informations de destinataire d’un fournisseur de carnet d’adresses dans le profil actif ; Les fournisseurs de carnets d’adresses peuvent avoir un ou plusieurs conteneurs de carnets d’adresses. |
|Pièce jointe  <br/> |Contient des données supplémentaires, telles qu’un fichier ou un objet OLE, à associer à un message. |
|Contrôle  <br/> |Active ou désactive un bouton et lance le traitement lorsque vous cliquez sur le bouton. |
|Liste de distribution  <br/> |Décrit un regroupement de destinataires de messages individuels. |
|Folder  <br/> |Contient des messages et d’autres conteneurs de messages. |
|Ouverture de session  <br/> |Gère la notification d’événements du fournisseur de services et les demandes des clients. |
|Utilisateur de messagerie  <br/> |Décrit un destinataire individuel d’un message. |
|Message  <br/> |Contient des informations qui peuvent être envoyées à un ou plusieurs destinataires. |
|Magasin de messages  <br/> |Agit comme une base de données de messages organisée hiérarchiquement. |
|Fournisseur  <br/> |Gère le démarrage et l’arrêt du fournisseur de services. |
|Spooler hook  <br/> |Effectue un traitement spécial sur les messages entrants et sortants. |
|Statut  <br/> |Fournit l’accès à l’état du fournisseur de services. |
|Tableau  <br/> |Fournit l’accès à une vue récapitulative des données d’objet au format de ligne et de colonne, similaire à une table de base de données. |
   
Tous les fournisseurs de services implémentent un objet fournisseur et un objet d’ouverture de session. Les objets fournisseur sont strictement destinés à la comptabilité; ils sont utilisés par MAPI pour contrôler les processus de démarrage et d’arrêt. Les objets d’ouverture de session s’adressent indirectement à certaines demandes clientes. Par exemple, l’objet d’ouverture de session du fournisseur de magasin de messages gère l’inscription des notifications et les demandes d’ouverture des objets du magasin de messages. 
  
Les objets fournisseur et d’ouverture de session implémentent une interface différente en fonction du type de fournisseur de services qui fournit l’implémentation. Un fournisseur de magasin de messages implémente les interfaces [IMSProvider : IUnknown](imsprovideriunknown.md) et [IMSLogon : IUnknown](imslogoniunknown.md) dans son fournisseur et ses objets d’ouverture de session, un fournisseur de carnet d’adresses implémente les interfaces [IABProvider : IUnknown](iabprovideriunknown.md) et [IABLogon : IUnknown](iablogoniunknown.md) , et un fournisseur de transport implémente les interfaces [IXPProvider : IUnknown](ixpprovideriunknown.md) et [IXPLogon : IUnknown](ixplogoniunknown.md) . 
  
Les fournisseurs de hook de messages implémentent des objets spooler hook ou des objets qui filtrent les messages entrants et sortants.
  
En règle générale, les fournisseurs de services n’utilisent que quelques objets. Le plus souvent, ils utilisent un objet de support fourni par MAPI pour aider à implémenter les demandes des clients. L’objet de support est personnalisé pour le type de fournisseur qui l’utilise. Pour tous les fournisseurs de services, l’objet de support inclut des méthodes de gestion des notifications d’événements, d’affichage des propriétés de configuration, d’ouverture d’objets et de gestion des erreurs. Le reste des méthodes sont spécifiques à son utilisation ; il existe des versions personnalisées pour le carnet d’adresses, le magasin de messages et les fournisseurs de transport, ainsi que pour la prise en charge de la configuration. Par exemple, l’objet de prise en charge du carnet d’adresses affiche les détails et les boîtes de dialogue des destinataires personnalisés. L’objet de support du magasin de messages prend en charge les opérations de copie et de déplacement pour les dossiers et les messages. L’objet de prise en charge du fournisseur de transport inclut des méthodes permettant de faciliter l’interaction avec le spouleur MAPI. 
  
Certains fournisseurs de services utilisent des données de table et des objets de données de propriété ( objets utilitaires implémentées par MAPI). Les objets de données de table permettent aux fournisseurs de services de gérer les données sous-jacentes d’une table. Les objets de données de propriété permettent aux fournisseurs de services de définir l’accès aux objets et aux propriétés. 
  
Les fournisseurs de transport qui prennent en charge le format TNEF (Transport Neutral Encapsulation Format) pour le transfert de propriétés utilisent un objet TNEF implémenté par MAPI pour prendre en charge l’interface [ITnef : IUnknown](itnefiunknown.md) . Pour plus d’informations, consultez [Développer un fournisseur de transport TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Voir aussi



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Développement d’un fournisseur de transport TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md)

