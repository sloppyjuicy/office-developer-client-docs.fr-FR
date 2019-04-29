---
title: Objets du fournisseur de services MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0976e986a33d8b96366a84527f227bd05ef7845e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432267"
---
# <a name="mapi-service-provider-objects"></a>Objets du fournisseur de services MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services implémentent de nombreux objets. Certains sont utilisés principalement par MAPI et d'autres sont utilisés par les applications clientes. Un petit nombre d'objets est implémenté par tous les types de fournisseurs de services; les autres sont spécifiques à un type de fournisseur unique. Le tableau suivant décrit tous les objets du fournisseur de services.
  
|**Objet fournisseur de services**|**Description**|
|:-----|:-----|
|Conteneur de carnet d'adresses  <br/> |Contient des informations sur les destinataires d'un fournisseur de carnets d'adresses dans le profil actif; les fournisseurs de carnets d'adresses peuvent avoir un ou plusieurs conteneurs de carnet d'adresses.  <br/> |
|Pièce jointe  <br/> |Contient des données supplémentaires, telles qu'un fichier ou un objet OLE, à associer à un message.  <br/> |
|Contrôle  <br/> |Active ou désactive un bouton et lance le traitement lorsque l'utilisateur clique sur le bouton.  <br/> |
|Liste de distribution  <br/> |Décrit un regroupement de destinataires de message individuels.  <br/> |
|Folder  <br/> |Contient des messages et d'autres conteneurs de messages.  <br/> |
|Ouverture de session  <br/> |Gère la notification d'événement du fournisseur de services et les demandes des clients.  <br/> |
|Utilisateur de messagerie  <br/> |Décrit un destinataire individuel d'un message.  <br/> |
|Message  <br/> |Contient des informations qui peuvent être envoyées à un ou plusieurs destinataires.  <br/> |
|Banque de messages  <br/> |Fait office de base de données organisée de manière hiérarchique.  <br/> |
|Fournisseur  <br/> |Gère le démarrage et l'arrêt du fournisseur de services.  <br/> |
|Hook spouleur  <br/> |Effectue un traitement spécial sur les messages entrants et sortants.  <br/> |
|Statut  <br/> |Permet d'accéder à l'état du fournisseur de services.  <br/> |
|Table  <br/> |Permet d'accéder à une vue récapitulative des données d'objet dans le format de ligne et de colonne, semblable à une table de base de données.  <br/> |
   
Tous les fournisseurs de services implémentent un objet Provider et un objet Logon. Les objets de fournisseur sont strictement destinés à la comptabilité; elles sont utilisées par MAPI pour contrôler les processus de démarrage et d'arrêt. Les objets d'ouverture de session dénombrent indirectement les demandes des clients. Par exemple, l'objet de connexion du fournisseur de banque de messages gère l'enregistrement des notifications et les demandes d'ouverture des objets de banque de messages. 
  
Les objets fournisseur et ouverture de session implémentent une interface différente selon le type de fournisseur de services qui fournit l'implémentation. Un fournisseur de banque de messages implémente les interfaces [IMSProvider: IUnknown](imsprovideriunknown.md) et [IMSLogon: IUnknown](imslogoniunknown.md) dans ses objets fournisseur et d'ouverture de session, un fournisseur de carnet d'adresses implémente l' [IABProvider: IUnknown](iabprovideriunknown.md) et [IABLogon: IUnknown](iablogoniunknown.md) les interfaces et un fournisseur de transport implémentent les interfaces [IXPProvider: IUnknown](ixpprovideriunknown.md) et [IXPLogon: IUnknown](ixplogoniunknown.md) . 
  
Les fournisseurs de raccordement de message implémentent des objets hook de spouleur ou des objets qui filtrent les messages entrants et sortants.
  
Les fournisseurs de services utilisent généralement seulement quelques objets. Ils utilisent le plus souvent un objet de prise en charge fourni par MAPI pour aider à implémenter les demandes des clients. L'objet support est personnalisé pour le type de fournisseur qui l'utilise. Pour tous les fournisseurs de services, l'objet support inclut des méthodes pour la gestion des notifications d'événements, l'affichage des propriétés de configuration, l'ouverture d'objets et la gestion des erreurs. Les autres méthodes sont propres à son utilisation; Il existe des versions personnalisées pour les carnets d'adresses, les banques de messages et les fournisseurs de transport, et pour la prise en charge de la configuration. Par exemple, l'objet de prise en charge du carnet d'adresses affiche des boîtes de dialogue détails et destinataires personnalisés. L'objet support de la Banque de messages prend en charge les opérations de copie et de déplacement pour les dossiers et les messages. L'objet de prise en charge de fournisseur de transport inclut des méthodes pour faciliter l'interaction avec le spouleur MAPI. 
  
Certains fournisseurs de services utilisent des données de table et des objets de données de propriété — objets utilitaires implémentés par MAPI. Les objets de données de tableau permettent aux fournisseurs de services de gérer les données sous-jacentes d'un tableau. Les objets de données de propriété permettent aux fournisseurs de services de définir l'accès aux objets et aux propriétés. 
  
Les fournisseurs de transport qui prennent en charge le format TNEF (Transport Neutral Encapsulation Format) pour le transfert des propriétés utilisent un objet TNEF que MAPI implémente pour prendre en charge l'interface [ITnef: IUnknown](itnefiunknown.md) . Pour plus d'informations, consultez [la rubrique développement d'un fournisseur de transport avec TNEF](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Voir aussi



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Développement d'un fournisseur de transport compatible TNEF](developing-a-tnef-enabled-transport-provider.md)

