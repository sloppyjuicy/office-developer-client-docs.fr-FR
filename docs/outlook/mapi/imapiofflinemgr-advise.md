---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426918"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit un client pour recevoir des rappels sur un objet hors connexion.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
>  [in] Indicateurs qui modifient le comportement. Seule la valeur MAPIOFFLINE_ADVISE_DEFAULT est prise en charge. 
    
 _pAdviseInfo_
  
> [in] Informations sur le type de rappel, le moment où recevoir un rappel, une interface de rappel pour l’appelant et d’autres détails. Il contient également un jeton client qui Outlook lors de l’envoi de rappels de notification ultérieurs à l’appelant client.
    
 _péAdviseToken_
  
> [out] Jeton de conseil renvoyé à l’appelant client pour annuler ultérieurement le rappel de l’objet.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’appel a réussi.
    
E_INVALIDARG
  
> Un paramètre non valide a été spécifié.
    
E_NOINTERFACE
  
> Interface de rappel spécifiée dans  *pAdviseInfo*  non valide. 
    
## <a name="remarks"></a>Remarques

Lors de l’ouverture d’un objet hors connexion à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client obtient un objet hors connexion qui prend en charge **IMAPIOfflineMgr**. Le client peut vérifier les types de rappels pris en charge par l’objet à l’aide de **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. Le client peut déterminer le type et d’autres détails sur le rappel qu’il souhaite, puis appeler **IMAPIOfflineMgr::Advise** pour recevoir ces rappels sur l’objet. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

