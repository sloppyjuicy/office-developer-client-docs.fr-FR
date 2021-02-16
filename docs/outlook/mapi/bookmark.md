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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 069cb41ceac70a2eaaa08440e43745605890f071
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418133"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit les données de signets pour la mémoire d’une position dans un tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Méthodes associées :  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Remarques

MAPI définit trois signets, répertoriés comme suit :
  
BOOKMARK_BEGINNING 
  
> Mémoriser la position de départ du tableau. 
    
BOOKMARK_CURRENT 
  
> Se souvenir de la position actuelle du tableau.
    
BOOKMARK_END 
  
> Mémoriser la position de fin du tableau.
    
Les clients peuvent créer d’autres signets pour mémoriser d’autres positions de tableau. Les signets ne sont valides que lorsque la table est ouverte. Les clients doivent libérer les signets qu’ils ont créés avant de fermer la table associée. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Types de données MAPI](mapi-data-types.md)

