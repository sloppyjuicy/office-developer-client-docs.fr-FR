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
ms.openlocfilehash: e0c8c4c6251581506c7bdd78c009bb12e8291c81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586934"
---
# <a name="imapiofflinemgradvise"></a>IMAPIOfflineMgr::Advise

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Enregistre un client pour recevoir des rappels sur un objet en mode hors connexion.
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
>  [in] Indicateurs qui modifient le comportement. Seule la valeur MAPIOFFLINE_ADVISE_DEFAULT est pris en charge. 
    
 _pAdviseInfo_
  
> [in] Informations sur le type de rappel, quand recevoir un rappel, une interface de rappel pour l’appelant et d’autres détails. Il contient également un jeton client par l’envoi de rappels de notification suivants à l’appelant client Outlook.
    
 _pulAdviseToken_
  
> [out] Un jeton advise est renvoyé à l’appelant de client d’annulation par la suite de rappel pour l’objet.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> L’appel a réussi.
    
E_INVALIDARG
  
> Un paramètre non valide a été spécifié.
    
E_NOINTERFACE
  
> L’interface de rappel spécifié dans *pAdviseInfo* n’est pas valide. 
    
## <a name="remarks"></a>Remarques

À l’ouverture d’un objet en mode hors connexion à l’aide de **[HrOpenOfflineObj](hropenofflineobj.md)**, un client obtient un objet en mode hors connexion qui prend en charge **IMAPIOfflineMgr**. Le client peut vérifier les types de rappels pris en charge par l’objet à l’aide de **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. Le client peut déterminer le type et autres détails sur le rappel il souhaite et ensuite appeler **IMAPIOfflineMgr::Advise** s’inscrire pour recevoir ces rappels sur l’objet. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)
  
[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)


[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)

