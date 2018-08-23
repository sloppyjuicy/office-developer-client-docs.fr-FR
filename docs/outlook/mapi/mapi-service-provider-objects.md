---
title: Objets du fournisseur de services MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 85a67216822360bcaf9544389f79980891951757
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584855"
---
# <a name="mapi-service-provider-objects"></a>Objets du fournisseur de services MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Nombre d’objets implémentés par les fournisseurs de service. Certains sont utilisées principalement par MAPI et certains sont utilisés par les applications clientes. Certains objets sont implémentées par tous les types de fournisseurs de services ; les autres sont spécifiques à un type de fournisseur unique. Le tableau suivant décrit tous les objets de fournisseur de service.
  
|**Objet fournisseur de services**|**Description**|
|:-----|:-----|
|Conteneur de carnet d’adresses  <br/> |Contient des informations de destinataires pour un fournisseur de carnet d’adresses dans le profil actif ; fournisseurs de carnet d’adresses peuvent avoir un ou plusieurs conteneurs de carnet d’adresses.  <br/> |
|Pièce jointe  <br/> |Contient des données supplémentaires, comme un fichier ou un objet OLE, à associer à un message.  <br/> |
|Contrôle  <br/> |Active ou désactive un bouton et démarre lorsque l’utilisateur clique sur le bouton de traitement.  <br/> |
|Liste de distribution  <br/> |Décrit un ensemble de destinataires de messages individuels.  <br/> |
|Folder  <br/> |Contient des messages et autres conteneurs de message.  <br/> |
|Logon  <br/> |Les poignées de demandes fournisseur événement notification et le client.  <br/> |
|Utilisateur de messagerie  <br/> |Décrit un destinataire d’un message individuel.  <br/> |
|Message  <br/> |Contient des informations qui peuvent être envoyées à un ou plusieurs destinataires.  <br/> |
|Banque de messages  <br/> |Agit comme une base de données organisé hiérarchiquement des messages.  <br/> |
|Provider  <br/> |Les poignées de l’arrêt et démarrage du fournisseur de service.  <br/> |
|Crochet spouleur  <br/> |Effectue un traitement spécial sur les messages entrants et sortants.  <br/> |
|Status  <br/> |Fournit l’accès à l’état du fournisseur de services.  <br/> |
|Table  <br/> |Permet d’accéder à un affichage de synthèse des données d’objet dans un format de ligne et de colonne, similaire à une table de base de données.  <br/> |
   
Tous les fournisseurs de services de mettre en œuvre un objet de fournisseur et un objet d’ouverture de session. Objets du fournisseur sont strictement pour référence ; ils sont utilisés par MAPI pour contrôler le processus de démarrage et arrêt. Objets d’ouverture de session du service indirectement certaines demandes des clients. Par exemple, le message stocker enregistrement de notification du fournisseur poignées de l’objet d’ouverture de session et les demandes pour ouvrir des objets de banque de messages. 
  
Objets de fournisseur et d’ouverture de session implémentent une interface différente en fonction du type de fournisseur de services qui fournit l’implémentation. Implémente un fournisseur de magasin de message la [IMSProvider : IUnknown](imsprovideriunknown.md) et [IMSLogon : IUnknown](imslogoniunknown.md) du carnet d’interfaces dans son fournisseur et objets d’ouverture de session, une adresse de fournisseur implémente la [IABProvider : IUnknown](iabprovideriunknown.md) et [IABLogon : IUnknown](iablogoniunknown.md) implémente des interfaces et un fournisseur de transport la [IXPProvider : IUnknown](ixpprovideriunknown.md) et [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces. 
  
Objets de raccordement spouleur ou des objets qui filtrent les messages entrants et sortants implémentés par les fournisseurs de raccordement de message.
  
Fournisseurs de services utilisent généralement que quelques objets. Fréquemment, qu’ils utilisent un objet de prise en charge MAPI fournit pour vous aider à implémenter les demandes des clients. Le type de fournisseur qui est à l’aide de l’objet de prise en charge est personnalisé. Pour tous les fournisseurs de services, l’objet de prise en charge inclut des méthodes pour la gestion de notification d’événement, en affichant les propriétés de configuration, les objets de l’ouverture et gestion des erreurs. Le reste des méthodes sont spécifiques à son utilisation ; Il existe des versions personnalisées pour le carnet d’adresses, banque de messages et les fournisseurs de transport et prise en charge de la configuration. Par exemple, l’objet de prise en charge du carnet d’adresses affiche les détails et boîtes de dialogue destinataires personnalisées. La banque de messages prennent en charge d’objet prend en charge la copie et le déplacement de dossiers et les messages. L’objet de prise en charge du fournisseur de transport inclut des méthodes pour faciliter l’interaction avec le spouleur MAPI. 
  
Certains fournisseurs de services utilisent des objets de données de table de données et la propriété : objets utilitaires implémentés par MAPI. Objets de données de table activer les fournisseurs de services gérer les données sous-jacentes d’un tableau. Objets de données de propriété Activer les fournisseurs de services définir l’objet et la propriété accès. 
  
Fournisseurs de transport qui prennent en charge le Transport Neutral Encapsulation Format TNEF () pour le transfert de propriétés utilisent un objet TNEF implémentés par MAPI pour prendre en charge la [ITnef : IUnknown](itnefiunknown.md) interface. Pour plus d’informations, voir [développement d’un fournisseur de Transport TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Voir aussi



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Développement d’un fournisseur de transport TNEF](developing-a-tnef-enabled-transport-provider.md)

