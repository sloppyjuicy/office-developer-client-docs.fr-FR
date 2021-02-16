---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413380"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère les objets associés à une session d’ouverture de session MAPI.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Exposé par :  <br/> |Objets de session  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPISession  <br/> |
|Type de pointeur :  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de session précédente.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Permet d’accéder à la table de la boutique de messages qui contient des informations sur tous les magasins de messages dans le profil de session.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Ouvre une magasin de messages et renvoie un pointeur [IMsgStore](imsgstoreimapiprop.md) pour un accès supplémentaire.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Ouvre le carnet d’adresses intégré MAPI, en renvoyant un [pointeur IAddrBook](iaddrbookimapiprop.md) pour un accès supplémentaire.  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Ouvre une section du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Permet d’accéder à la table d’état, une table qui contient des informations sur toutes les ressources MAPI de la session.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Ouvre un objet et renvoie un pointeur d’interface pour un accès supplémentaire.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet.  <br/> |
|[Conseiller](imapisession-advise.md) <br/> |S’inscrit pour recevoir une notification des événements spécifiés qui affectent la session.  <br/> |
|[Unadvise](imapisession-unadvise.md) <br/> |Annule l’envoi de notifications précédemment définies avec un appel à la **méthode Advise.**  <br/> |
|**MessageOptions** <br/> | *Non pris en charge ou documenté.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Non pris en charge ou documenté.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Déconseillé. Renvoie les types d’adresses qui peuvent être gérés par tous les fournisseurs de transport dans la session.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Renvoie l’identificateur d’entrée de l’objet qui fournit l’identité principale de la session.  <br/> |
|[Logoff](imapisession-logoff.md) <br/> |Met fin à une session MAPI.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Établit une magasin de messages comme magasin de messages par défaut pour la session.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Renvoie un [pointeur IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications aux services de message.  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |Affiche un formulaire.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Crée un jeton numérique que la **méthode ShowForm** utilise pour accéder à un message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

