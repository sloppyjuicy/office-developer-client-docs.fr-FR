---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405092"
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
  
> dans Nombre d'octets dans l'ID d'entrée du message.
    
 _lpeid_
  
> dans ID d'entrée du message.
    
 _PPV_
  
>  [in]/[out] pointeur vers la structure **[HDRSYNC](hdrsync.md)** pour l'en-tête de message. 
    
## <a name="remarks"></a>Remarques

Sur **IOSTX:: SyncHdrBeg**, le magasin local passe à l' [État d'en-tête du message de téléchargement](download-message-header-state.md). Outlook initialise pour le client la structure **HDRSYNC** avec la représentation actuelle de l'en-tête du message dans le magasin et le dossier parent. Le client doit ensuite télécharger un élément de message complet (en tant que *pmsgFull* dans **HDRSYNC** ). Si cette opération réussit, le client définit également *ulFlags* dans **HDRSYNC** en tant que **HSF_OK**. Sur **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)**, Outlook vérifie le résultat dans **HDRSYNC** et utilise les informations de **HDRSYNC** pour mettre à jour l'en-tête de message local. 
  
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

