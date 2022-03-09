---
title: IOSTXSyncHdrEnd
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
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: bda01071c44795b4f521443930b9eee8ee5b8cc9
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381473"
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
  
> [in] **[Interface IMAPIProgress pour](imapiprogressiunknown.md)** la synchronisation des messages déplacés ou copiés. Voir mapidefs.h pour la définition de type **de LPMAPIPROGRESS**.

## <a name="remarks"></a>Remarques

Sur **[IOSTX::SyncBeg](iostx-syncbeg.md)**, la boutique locale entre dans l’état d’en-tête [du message de téléchargement](download-message-header-state.md). Le client télécharge un élément de message complet (comme _pmsgFull_ dans **[HDRSYNC](hdrsync.md)** ). Si cela réussit, le client définit également _ulFlags_ dans **HDRSYNC** comme **HSF_OK**. Sur **IOSTX::SyncHdrEnd**, Outlook vérifie le résultat dans **HDRSYNC** et utilise _pprog_ et les informations dans **HDRSYNC** pour mettre à jour l’en-tête de message local.
  
Le magasin local revient à l’état dans le précédent **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.
  
## <a name="see-also"></a>Voir aussi

[IOSTX::GetLastError](iostx-getlasterror.md)  
[IOSTX::InitSync](iostx-initsync.md)  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)  
[IOSTX::SyncBeg](iostx-syncbeg.md)  
[IOSTX::SyncEnd](iostx-syncend.md)  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)  
[IOSTX : IUnknown](iostxiunknown.md)
 [Constantes MAPI](mapi-constants.md)
