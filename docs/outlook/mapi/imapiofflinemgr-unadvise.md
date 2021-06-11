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
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404854"
---
# <a name="imapiofflinemgrunadvise"></a>IMAPIOfflineMgr::Unadvise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Annule les rappels pour un objet hors connexion.
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Indicateurs pour l’annulation du rappel. Seule la valeur MAPIOFFLINE_UNADVISE_DEFAULT est prise en charge.
    
 _ulAdviseToken_
  
> [in] Jeton de conseil qui identifie l’inscription de rappel à annuler. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> L’appel a réussi. Cet appel doit renvoyer S_OK.
    
## <a name="remarks"></a>Remarques

Supprime l’inscription pour le rappel qui était associé à  *ulAdviseToken*  renvoyé à partir d’un appel précédent à **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Fait que **l’objet IMAPIOfflineMgr** libère sa référence sur l’objet **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associé  *à ulAdviseToken*  . 
  
## <a name="see-also"></a>Voir aussi



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Constantes MAPI](mapi-constants.md)

