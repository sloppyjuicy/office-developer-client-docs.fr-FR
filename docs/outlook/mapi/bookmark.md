---
title: BOOKMARK
description: Décrit la syntaxe et les remarques relatives à BOOKMARK, qui définit les données des signets pour la mémorisation d’une position dans une table.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
ms.openlocfilehash: 4af44ffca66e94f8ce32198584181caf71cb2230
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770431"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit les données de signets pour la mémorisation d’une position dans une table. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Méthodes associées :  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Remarques

MAPI définit trois signets, répertoriés comme suit :
  
BOOKMARK_BEGINNING 
  
> Mémorise la position de départ de la table. 
    
BOOKMARK_CURRENT 
  
> Se souvient de la position actuelle de la table.
    
BOOKMARK_END 
  
> Se souvient de la position de fin de la table.
    
Les clients peuvent créer d’autres signets pour mémoriser d’autres positions de table. Les signets sont valides uniquement lorsque la table est ouverte. Les clients doivent libérer les signets qu’ils ont créés avant de fermer la table associée. 
  
## <a name="see-also"></a>Voir aussi



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[Types de données MAPI](mapi-data-types.md)

