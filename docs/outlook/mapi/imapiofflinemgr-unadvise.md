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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 35dfc7af9852609dcfcc3fcb9d65ec2e4afa9632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579521"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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

