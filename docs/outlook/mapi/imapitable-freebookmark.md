---
title: IMAPITableFreeBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FreeBookmark
api_type:
- COM
ms.assetid: 797833f7-8295-41bc-8980-977e5f5e05e8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a1ad209ff127a34d7da5ca8dbe1f4a6656d32876
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409453"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Libère la mémoire associée à un signet.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Parameters

 _bkPosition_
  
> [in] Signet à libérer, créé en appelant la [méthode IMAPITable::CreateBookmark.](imapitable-createbookmark.md) 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le signet a été libéré.
    
MAPI_E_INVALID_BOOKMARK 
  
> Le signet spécifié n’existe pas.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPITable::FreeBookmark** libère un signet qui n’est plus nécessaire. Le signet n’est plus valide après cet appel. Chaque fois qu’un tableau est libéré de la mémoire, tous ses signets associés sont également libérés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si l’appelant passe l’un des trois signets prédéfincis dans le paramètre  _bkPosition,_ ignorez la demande et renvoyez S_OK. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

