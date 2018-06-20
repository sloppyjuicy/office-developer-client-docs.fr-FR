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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d6621e2bcd7831016efd7ac43f93ef83aaf41c29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784084"
---
# <a name="imapitablefreebookmark"></a>IMAPITable::FreeBookmark

  
  
**S’applique à**: Outlook 
  
Libère la mémoire associée à un signet.
  
```cpp
HRESULT FreeBookmark(
BOOKMARK bkPosition
);
```

## <a name="parameters"></a>Paramètres

 _bkPosition_
  
> [in] Le signet afin d’être libérée, créé en appelant la méthode [IMAPITable::CreateBookmark](imapitable-createbookmark.md) . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le signet a été libéré avec succès.
    
MAPI_E_INVALID_BOOKMARK 
  
> Le signet spécifié n’existe pas.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPITable::FreeBookmark** libère un signet qui n’est plus nécessaire. Le signet n’est plus valide après cet appel. Chaque fois qu’une table est libérée de la mémoire, tous ses signets associés sont également libérées. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si l’appelant transmet une des trois signets prédéfinis dans le paramètre _bkPosition_ , ignorer la demande et qu’elles retournent S_OK. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

