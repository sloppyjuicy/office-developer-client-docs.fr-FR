---
title: IOSTXSyncHdrEnd
description: Décrit la syntaxe, les paramètres et les remarques pour IOSTX SyncHdrEnd, qui met fin à la synchronisation d’un en-tête de message.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
ms.openlocfilehash: ab314a0808a29596a2f8f948639aab1616ef4370
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828538"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

**S’applique à** : Outlook 2013 | Outlook 2016
  
Met fin à la synchronisation d’un en-tête de message.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Paramètres

 _pprog_
  
> [in] **[Interface IMAPIProgress](imapiprogressiunknown.md)** pour la synchronisation des messages déplacés ou copiés. Consultez mapidefs.h pour connaître la définition de type de **LPMAPIPROGRESS**.

## <a name="remarks"></a>Remarques

Sur **[IOSTX::SyncBeg](iostx-syncbeg.md)**, le magasin local entre dans [l’état d’en-tête du message de téléchargement](download-message-header-state.md). Le client télécharge un élément de message complet (sous la forme _pmsgFull_ dans **[HDRSYNC](hdrsync.md)** ). Si cette opération réussit, le client définit également _ulFlags_ dans **HDRSYNC** comme **HSF_OK**. Sur **IOSTX::SyncHdrEnd**, Outlook vérifie le résultat dans **HDRSYNC** et utilise _pprog_ et les informations dans **HDRSYNC** pour mettre à jour l’en-tête de message local.
  
Le magasin local revient à l’état dans lequel il se trouvait avant **[l’IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** précédent.
  
## <a name="see-also"></a>Voir aussi

[IOSTX::GetLastError](iostx-getlasterror.md)  
[IOSTX::InitSync](iostx-initsync.md)  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)  
[IOSTX::SyncBeg](iostx-syncbeg.md)  
[IOSTX::SyncEnd](iostx-syncend.md)  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)  
[IOSTX : IUnknown](iostxiunknown.md)
 [Constantes MAPI](mapi-constants.md)
