---
title: IMAPISession IUnknown
description: Décrit les propriétés et l’ordre de vtable des membres pour IMAPISessionIUnknown, qui gère les objets associés à une session d’ouverture de session MAPI.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
ms.openlocfilehash: 7a717cbf2d75ffe1f3588f20e586705680639655
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827911"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère les objets associés à une session d’ouverture de session MAPI.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Exposé par :  <br/> |Objets de session  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPISession  <br/> |
|Type de pointeur :  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[Getlasterror](imapisession-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de session précédente. |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Fournit l’accès à la table du magasin de messages qui contient des informations sur tous les magasins de messages dans le profil de session. |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Ouvre un magasin de messages et retourne un pointeur [IMsgStore](imsgstoreimapiprop.md) pour un accès supplémentaire. |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Ouvre le carnet d’adresses intégré MAPI, en retournant un pointeur [IAddrBook](iaddrbookimapiprop.md) pour un accès supplémentaire. |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Fournit l’accès à la table d’état, une table qui contient des informations sur toutes les ressources MAPI de la session. |
|[OpenEntry](imapisession-openentry.md) <br/> |Ouvre un objet et retourne un pointeur d’interface pour un accès supplémentaire. |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet. |
|[Conseiller](imapisession-advise.md) <br/> |S’inscrit pour recevoir une notification des événements spécifiés qui affectent la session. |
|[Non-surveillance](imapisession-unadvise.md) <br/> |Annule l’envoi de notifications précédemment configurées avec un appel à la méthode **Advise** . |
|**MessageOptions** <br/> | *Non pris en charge ou documenté.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Non pris en charge ou documenté.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Déconseillé. Retourne les types d’adresses qui peuvent être gérés par tous les fournisseurs de transport de la session. |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Retourne l’identificateur d’entrée de l’objet qui fournit l’identité principale de la session. |
|[Logoff](imapisession-logoff.md) <br/> |Met fin à une session MAPI. |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Établit un magasin de messages comme magasin de messages par défaut pour la session. |
|[AdminServices](imapisession-adminservices.md) <br/> |Retourne un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications aux services de messages. |
|[ShowForm](imapisession-showform.md) <br/> |Affiche un formulaire. |
|[PrepareForm](imapisession-prepareform.md) <br/> |Crée un jeton numérique que la méthode **ShowForm** utilise pour accéder à un message. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

