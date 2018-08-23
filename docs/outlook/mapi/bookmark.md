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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: be41a9916b6b231d5715cf18fe2b0d804434f2ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594480"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Définit les données de signets pour mémoriser une position dans un tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Méthodes associées :  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Remarques

MAPI définit trois signets, répertoriés comme suit :
  
BOOKMARK_BEGINNING 
  
> Mémorise la position de départ de la table. 
    
BOOKMARK_CURRENT 
  
> Mémorise la position actuelle de la table.
    
BOOKMARK_END 
  
> Mémorise la position de fin de la table.
    
Clients peuvent créer d’autres signets mémorisation des autres positions de tableau. Les signets ne sont valides que si la table est ouverte. Clients doivent libérer tous les signets qu’ils ont créés avant la fermeture de la table associée. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Types de données MAPI](mapi-data-types.md)

