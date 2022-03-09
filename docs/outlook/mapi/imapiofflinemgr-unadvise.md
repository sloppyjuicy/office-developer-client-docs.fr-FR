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
ms.openlocfilehash: 2bdf81de8e14a79d4a18274988160e73f6d30b1a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369384"
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

Supprime l’inscription pour le rappel qui était associé à _ulAdviseToken_ renvoyé à partir d’un appel précédent à **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Fait que **l’objet IMAPIOfflineMgr** libère sa référence sur l’objet **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associé _à ulAdviseToken_.
  
## <a name="see-also"></a>Voir aussi

[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
 [Constantes MAPI](mapi-constants.md)
