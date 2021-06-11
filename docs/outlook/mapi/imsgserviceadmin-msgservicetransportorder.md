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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420093"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a>IMsgServiceAdmin::MsgServiceTransportOrder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit l’ordre dans lequel les fournisseurs de transport sont appelés pour remettre un message.
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parameters

 _cUID_
  
> [in] Nombre d’identificateurs uniques dans le _paramètre lpUIDList._ 
    
 _lpUIDList_
  
> [in] Pointeur vers un tableau d’identificateurs uniques qui représentent des fournisseurs de transport. Le tableau contient un identificateur pour chaque fournisseur de transport configuré dans le profil actuel.
    
 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’ordre de transport a été correctement établi.
    
MAPI_E_BUSY 
  
> La valeur du  _paramètre cUID_ diffère du nombre de fournisseurs de transport dans le profil. 
    
MAPI_E_NOT_FOUND 
  
> Une ou plusieurs structures [MAPIUID](mapiuid.md) transmises dans le paramètre  _lpUIDList_ ne font pas référence à un fournisseur de transport actuellement dans le profil. 
    
## <a name="remarks"></a>Remarques

La **méthode IMsgServiceAdmin::MsgServiceTransportOrder** définit l’ordre de remise des fournisseurs de transport dans un profil. Le paramètre _lpUIDList_ doit contenir une liste triée d’identificateurs d’entrée de fournisseur de transport obtenus à partir de la propriété **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) de la table renvoyée par la méthode [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md) Une application cliente doit transmettre la liste complète dans  _lpUIDList_.
  
 **SetTransportOrder** remplace les préférences de fournisseur de transport telles que l’indicateur STATUS_XP_PREFER_LAST définie dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)). 
  
## <a name="see-also"></a>Voir aussi



[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

