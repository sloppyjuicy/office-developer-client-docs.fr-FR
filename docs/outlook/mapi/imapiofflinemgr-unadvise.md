---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 29d6b7bf1e8bbb9d9fb1d5a17441fb779d9d67ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604865"
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

## <a name="parameters"></a>Paramètres

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

