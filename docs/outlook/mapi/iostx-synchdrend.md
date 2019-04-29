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
description: 'Dernière modification: 03 juillet 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432771"
---
# <a name="iostxsynchdrend"></a>IOSTX::SyncHdrEnd

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Met fin à la synchronisation pour un en-tête de message.
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a>Paramètres

 _pprog_
  
> dans Interface **[méthode imapiprogress](imapiprogressiunknown.md)** pour la synchronisation des messages déplacés ou copiés. Voir mapidefs. h pour la définition de type de **LPMAPIPROGRESS**. 
    
## <a name="remarks"></a>Remarques

Sur **[IOSTX:: SyncBeg](iostx-syncbeg.md)**, le magasin local entre l' [État de l'en-tête du message de téléchargement](download-message-header-state.md). Le client télécharge un élément de message complet (en tant que *pmsgFull* dans **[HDRSYNC](hdrsync.md)** ). Si cette opération réussit, le client définit également *ulFlags* dans **HDRSYNC** en tant que **HSF_OK**. Sur **IOSTX:: SyncHdrEnd**, Outlook vérifie le résultat dans **HDRSYNC** et utilise *Pprog* et les informations dans **HDRSYNC** pour mettre à jour l'en-tête de message local. 
  
La banque locale revient à l'État dans lequel elle se trouvait avant le précédent **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)**. 
  
## <a name="see-also"></a>Voir aussi



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Constantes MAPI](mapi-constants.md)

