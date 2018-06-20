---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5b96a45bab4cd00d23604d0b0b25f3e772277395
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784241"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**S’applique à**: Outlook 
  
Définit l’ordre dans les transports fournisseurs sont appelées pour remettre un message.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Paramètres

 _cUID_
  
> [in] Le nombre des identificateurs uniques dans le paramètre _lpUIDList_ . 
    
 _lpUIDList_
  
> [in] Pointeur vers un tableau d’identificateurs uniques qui représentent des fournisseurs de transport. Le tableau contient un identificateur pour chaque fournisseur de transport configurée dans le profil actif.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’ordre de transport a été défini avec succès.
    
MAPI_E_BUSY 
  
> La valeur dans le paramètre _cUID_ est différent du nombre de fournisseurs de transport réellement dans le profil. 
    
MAPI_E_NOT_FOUND 
  
> Une ou plusieurs des structures [MAPIUID](mapiuid.md) passés dans le paramètre _lpUIDList_ ne font pas référence à un fournisseur de transport actuellement dans le profil. 
    
## <a name="remarks"></a>Remarques

La méthode **IMsgServiceAdmin::MsgServiceTransportOrder** définit l’ordre de remise des fournisseurs de transport dans un profil. Le paramètre _lpUIDList_ doit contenir une liste triée des identificateurs d’entrée-fournisseur de transport obtenu à partir de la propriété **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) du tableau renvoyé par la [IMsgServiceAdmin :: GetProviderTable](imsgserviceadmin-getprovidertable.md) méthode. Une application cliente doit transmettre la liste complète de _lpUIDList_.
  
 Les substitutions **SetTransportOrder** transportent préférences fournisseur telles que l’indicateur STATUS_XP_PREFER_LAST défini dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

