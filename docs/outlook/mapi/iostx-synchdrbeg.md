---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
ms.openlocfilehash: ef4ec91b4719a9de0609ae0d753d88f2b26d336b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368599"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

**S’applique à** : Outlook 2013 | Outlook 2016
  
Démarre la synchronisation pour un en-tête de message.
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Paramètres

 _cbeid_
  
> [in] Nombre d’octets dans l’ID d’entrée du message.

 _lpeid_
  
> [in] ID d’entrée du message.

 _ppv_
  
> [in]/[out] Pointeur vers la structure **[HDRSYNC](hdrsync.md)** de l’en-tête de message.

## <a name="remarks"></a>Remarques

Sur **IOSTX::SyncHdrBeg**, le magasin local passe à l’état d’en-tête [du message de téléchargement](download-message-header-state.md). Outlook initialise pour le client la structure **HDRSYNC** avec la représentation actuelle de l’en-tête de message dans la boutique et le dossier parent. Le client doit ensuite télécharger un élément de message complet (comme _pmsgFull_ dans **HDRSYNC** ). Si cela a réussi, le client définit également _ulFlags_ dans **HDRSYNC** comme **HSF_OK**. Sur **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook vérifie le résultat dans **HDRSYNC** et utilise les informations dans **HDRSYNC** pour mettre à jour l’en-tête du message local.
  
## <a name="see-also"></a>Voir aussi

[IOSTX::GetLastError](iostx-getlasterror.md)  
[IOSTX::InitSync](iostx-initsync.md)  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)  
[IOSTX::SyncBeg](iostx-syncbeg.md)  
[IOSTX::SyncEnd](iostx-syncend.md)  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)  
[IOSTX : IUnknown](iostxiunknown.md)
 [Constantes MAPI](mapi-constants.md)
