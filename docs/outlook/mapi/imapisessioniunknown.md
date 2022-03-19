---
title: IMAPISession IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 633bc0c30b26cae54f464f7596fb8fbea47c96b1
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63627990"
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
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de session précédente. |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Permet d’accéder à la table de la boutique de messages qui contient des informations sur tous les magasins de messages dans le profil de session. |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Ouvre une magasin de messages et renvoie un pointeur [IMsgStore](imsgstoreimapiprop.md) pour un accès supplémentaire. |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Ouvre le carnet d’adresses intégré MAPI, en renvoyant un [pointeur IAddrBook](iaddrbookimapiprop.md) pour un accès supplémentaire. |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Ouvre une section du profil actuel et renvoie un [pointeur IProfSect](iprofsectimapiprop.md) pour un accès supplémentaire. |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Permet d’accéder à la table d’état, une table qui contient des informations sur toutes les ressources MAPI de la session. |
|[OpenEntry](imapisession-openentry.md) <br/> |Ouvre un objet et renvoie un pointeur d’interface pour un accès supplémentaire. |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet. |
|[Conseiller](imapisession-advise.md) <br/> |S’inscrit pour recevoir une notification des événements spécifiés qui affectent la session. |
|[Unadvise](imapisession-unadvise.md) <br/> |Annule l’envoi de notifications précédemment définies avec un appel à la **méthode Advise** . |
|**MessageOptions** <br/> | *Non pris en charge ou documenté.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Non pris en charge ou documenté.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Déconseillé. Renvoie les types d’adresses qui peuvent être gérés par tous les fournisseurs de transport dans la session. |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Renvoie l’identificateur d’entrée de l’objet qui fournit l’identité principale de la session. |
|[Logoff](imapisession-logoff.md) <br/> |Met fin à une session MAPI. |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Établit une magasin de messages comme magasin de messages par défaut pour la session. |
|[AdminServices](imapisession-adminservices.md) <br/> |Renvoie un [pointeur IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications aux services de message. |
|[ShowForm](imapisession-showform.md) <br/> |Affiche un formulaire. |
|[PrepareForm](imapisession-prepareform.md) <br/> |Crée un jeton numérique que la **méthode ShowForm** utilise pour accéder à un message. |
   
## <a name="see-also"></a>Consultez aussi



[Interfaces MAPI](mapi-interfaces.md)

