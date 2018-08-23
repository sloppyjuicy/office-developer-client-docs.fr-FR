---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Dernière modification : 03 juillet 2012'
ms.openlocfilehash: a40d4e62a930219a738c7b431f3d2192007c3d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591330"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fin de la synchronisation pour un en-tête de message.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Paramètres

 _pprog_
  
> [in] Interface **[IMAPIProgress](imapiprogressiunknown.md)** pour la synchronisation de déplacé ou copié des messages. Voir mapidefs.h pour la définition du type de **LPMAPIPROGRESS**. 
    
## <a name="remarks"></a>Remarques

Lors de l' **[IOSTX::SyncBeg](iostx-syncbeg.md)**, du stockage local passe l' [état d’en-tête de message du téléchargement](download-message-header-state.md). Le client télécharge un élément de message complète (comme *pmsgFull* dans **[HDRSYNC](hdrsync.md)** ). Si l’opération réussit, le client définit également *ulFlags* **HDRSYNC** en tant que **HSF_OK**. Fonction **IOSTX::SyncHdrEnd**, Outlook vérifie le résultat dans **HDRSYNC** et utilise *pprog* et les informations **HDRSYNC** pour mettre à jour l’en-tête de message local. 
  
Le magasin local renvoie à l’état, qu'il se trouvait avant précédente **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**. 
  
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

