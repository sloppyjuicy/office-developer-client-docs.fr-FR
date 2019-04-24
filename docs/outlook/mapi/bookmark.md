---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318038"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit les données de signets pour la mémorisation d'une position dans un tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Méthodes connexes:  <br/> |[IMAPITable:: CreateBookmark](imapitable-createbookmark.md) [IMAPITable:: FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Remarques

MAPI définit trois signets, comme suit:
  
BOOKMARK_BEGINNING 
  
> Mémorise la position de départ de la table. 
    
BOOKMARK_CURRENT 
  
> Mémorise la position actuelle de la table.
    
BOOKMARK_END 
  
> Mémorise la position de fin de la table.
    
Les clients peuvent créer d'autres signets pour mémoriser les autres positions des tables. Les signets ne sont valides que lorsque le tableau est ouvert. Les clients doivent libérer tous les signets qu'ils ont créés avant de fermer le tableau associé. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Types de donn�es MAPI](mapi-data-types.md)

