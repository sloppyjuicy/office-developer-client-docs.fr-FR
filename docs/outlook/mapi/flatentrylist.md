---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336896"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [FLATENTRY](flatentry.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>Members

**cEntries**
  
> Nombre de structures **FLATENTRY** dans le tableau décrit par le membre **abEntries** . 
    
**cbEntries**
  
> Nombre d'octets dans le tableau décrit par **abEntries**. 
    
**abEntries**
  
> Tableau d'octets contenant une ou plusieurs structures **FLATENTRY** , organisées de bout en bout. 
    
## <a name="remarks"></a>Remarques

Dans le tableau **abEntries** , chaque structure **FLATENTRY** est alignée sur une frontière naturellement alignée. Les octets supplémentaires sont inclus comme remplissage afin de s'assurer de l'alignement naturel entre deux structures **FLATENTRY** . La première structure **FLATENTRY** dans le tableau est toujours alignée correctement car l'offset du membre **abEntries** est égal à 8. Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée arrondie au multiple suivant de 4. Utilisez la macro [CbFLATENTRY](cbflatentry.md) pour calculer la taille d'une structure **FLATENTRY** . 
  
Par exemple, la deuxième structure **FLATENTRY** démarre à un offset qui se compose du décalage de la première entrée plus la longueur de la première entrée arrondie aux quatre octets suivants. La longueur de la première entrée est la longueur de son membre **CB** plus la longueur de son membre **abEntry** . 
  
L'exemple de code suivant indique comment calculer les décalages dans une structure **FLATENTRYLIST** . Supposons que _lpFlatEntry_ est un pointeur vers la première structure de la liste. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>Voir aussi

- [FLATENTRY](flatentry.md)
- [Propriété canonique PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)
- [Structures MAPI](mapi-structures.md)

