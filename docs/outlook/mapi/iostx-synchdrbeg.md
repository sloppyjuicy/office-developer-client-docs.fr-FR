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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a5c754a209a3e1bce8888851b88e116f92920eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784334"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**S’applique à**: Outlook 
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée du message.
    
 _lpeid_
  
> [in] L’identificateur d’entrée du message.
    
 _PPV_
  
>  [in] / [out] pointeur vers la structure **[HDRSYNC](hdrsync.md)** pour l’en-tête du message. 
    
## <a name="remarks"></a>Remarques

Lors de l' **IOSTX::SyncHdrBeg**, local stocker des transitions pour l' [état d’en-tête de message du téléchargement](download-message-header-state.md). Outlook initialise pour le client de la structure **HDRSYNC** avec la représentation actuelle de l’en-tête du message dans le magasin et le dossier parent. Le client doit télécharger puis un élément de message complète (comme *pmsgFull* dans **HDRSYNC** ). Si cela a réussi, le client définit également *ulFlags* **HDRSYNC** en tant que **HSF_OK**. Fonction **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook vérifie le résultat dans **HDRSYNC** et utilise les informations de **HDRSYNC** pour mettre à jour l’en-tête de message local. 
  
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

