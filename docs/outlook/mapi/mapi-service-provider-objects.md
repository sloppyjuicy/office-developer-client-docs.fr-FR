---
title: Objets du fournisseur de services MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b37d4c3ce4ee09f5efd9868575e6feba6c2f62d6
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781316"
---
# <a name="mapi-service-provider-objects"></a>Objets du fournisseur de services MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services implémentent de nombreux objets. Certaines sont utilisées principalement par MAPI et d’autres par les applications clientes. Quelques objets sont implémentés par tous les types de fournisseurs de services ; les autres sont spécifiques à un type de fournisseur unique. Le tableau suivant décrit tous les objets du fournisseur de services.
  
|**Objet fournisseur de services**|**Description**|
|:-----|:-----|
|Conteneur de carnet d’adresses  <br/> |Contient des informations sur le destinataire d’un fournisseur de carnet d’adresses dans le profil actif . Les fournisseurs de carnet d’adresses peuvent avoir un ou plusieurs conteneurs de carnet d’adresses. |
|Pièce jointe  <br/> |Contient des données supplémentaires, telles qu’un fichier ou un objet OLE, à associer à un message. |
|Contrôle  <br/> |Active ou désactive un bouton et lance le traitement lorsque l’utilisateur clique sur le bouton. |
|Liste de distribution  <br/> |Décrit un regroupement de destinataires de message individuels. |
|Folder  <br/> |Contient des messages et d’autres conteneurs de messages. |
|Ouverture de session  <br/> |Gère les notifications d’événements du fournisseur de services et les demandes clientes. |
|Utilisateur de messagerie  <br/> |Décrit un destinataire individuel d’un message. |
|Message  <br/> |Contient des informations qui peuvent être envoyées à un ou plusieurs destinataires. |
|Magasin de messages  <br/> |Agit comme une base de données de messages organisée hiérarchiquement. |
|Fournisseur  <br/> |Gère le démarrage et l’arrêt du fournisseur de services. |
|Hook Spooler  <br/> |Effectue un traitement spécial sur les messages entrants et sortants. |
|État  <br/> |Permet d’accéder à l’état du fournisseur de services. |
|Tableau  <br/> |Permet d’accéder à un affichage récapitulatif des données d’objet au format de ligne et de colonne, semblable à une table de base de données. |
   
Tous les fournisseurs de services implémentent un objet fournisseur et un objet d’accès. Les objets fournisseurs sont strictement pour le comptabilité ; Ils sont utilisés par MAPI pour contrôler les processus de démarrage et d’arrêt. Les objets d’logon service certaines demandes client indirectement. Par exemple, l’objet d’ouverture de messagerie du fournisseur de magasins de messages gère l’inscription des notifications et les demandes d’ouverture des objets de la boutique de messages. 
  
Les objets fournisseur et d’accès implémentent une interface différente en fonction du type de fournisseur de services qui fournit l’implémentation. Un fournisseur de magasin de messages implémente les interfaces [IMSProvider : IUnknown](imsprovideriunknown.md) et [IMSLogon : IUnknown](imslogoniunknown.md) dans ses objets fournisseur et de logon, un fournisseur de carnet d’adresses implémente [IABProvider : IUnknown](iabprovideriunknown.md) et [IABLogon : interfaces IUnknown](iablogoniunknown.md) , et un fournisseur de transport implémente les interfaces [IXPProvider : IUnknown](ixpprovideriunknown.md) et [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces. 
  
Les fournisseurs de hooks de message implémentent des objets hook depooler ou des objets qui filtrent les messages entrants et sortants.
  
Les fournisseurs de services utilisent généralement uniquement quelques objets. Le plus souvent, ils utilisent un objet de support que MAPI fournit pour vous aider à implémenter les demandes des clients. L’objet de support est personnalisé pour le type de fournisseur qui l’utilise. Pour tous les fournisseurs de services, l’objet de prise en charge inclut des méthodes de gestion des notifications d’événement, d’affichage des propriétés de configuration, d’ouverture d’objets et de gestion des erreurs. Le reste des méthodes sont spécifiques à son utilisation ; il existe des versions personnalisées pour les fournisseurs de carnet d’adresses, de magasin de messages et de transport, et pour la prise en charge de la configuration. Par exemple, l’objet de prise en charge du carnet d’adresses affiche des détails et des boîtes de dialogue de destinataire personnalisées. L’objet de support de la boutique de messages prend en charge les opérations de copie et de déplacement pour les dossiers et les messages. L’objet de support du fournisseur de transport inclut des méthodes pour faciliter l’interaction avec lepooler MAPI. 
  
Certains fournisseurs de services utilisent des données de table et des objets de données de propriétés , objets utilitaires implémentés par MAPI. Les objets de données de table permettent aux fournisseurs de services de gérer les données sous-jacentes d’une table. Les objets de données de propriété permettent aux fournisseurs de services de définir l’accès aux objets et aux propriétés. 
  
Les fournisseurs de transport qui utilisent le format TNEF (Transport Neutral Encapsulation Format) pour le transfert de propriétés utilisent un objet TNEF implémenté par MAPI pour prendre en charge l’interface [ITnef : IUnknown](itnefiunknown.md) . Pour plus d’informations, voir [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Voir aussi



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Développement d’un fournisseur TNEF-Enabled transport de données](developing-a-tnef-enabled-transport-provider.md)

