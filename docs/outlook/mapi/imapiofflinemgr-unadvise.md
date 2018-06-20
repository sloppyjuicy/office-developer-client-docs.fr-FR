---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b52dcd87c8714ad59db560a5ae4a8300f9cc83ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783877"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**S’applique à**: Outlook 
  
Annule des rappels pour un objet en mode hors connexion.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Indicateurs d’annulation de rappel. Seule la valeur MAPIOFFLINE_UNADVISE_DEFAULT est pris en charge.
    
 _ulAdviseToken_
  
> [in] Un jeton advise qui identifie l’inscription du rappel qui doit être annulée. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK
  
> L’appel a réussi. Cet appel doit renvoyer S_OK.
    
## <a name="remarks"></a>Remarques

Supprime l’inscription du rappel qui a été associé avec *ulAdviseToken* renvoyé à partir d’un appel précédent à **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Entraîne l’objet **IMAPIOfflineMgr** libérer sa référence à l’objet **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associé *ulAdviseToken* . 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Constantes MAPI](mapi-constants.md)

