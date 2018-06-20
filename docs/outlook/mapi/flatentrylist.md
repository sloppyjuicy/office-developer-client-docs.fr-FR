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
ms.openlocfilehash: a8f17c3cf3d3d00930f87acd004b24f683a3fc8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783317"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**S’applique à**: Outlook 
  
Contient un tableau de structures [FLATENTRY](flatentry.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a>Membres

**cEntries**
  
> Nombre de structures **FLATENTRY** dans le tableau indiqué par le membre **abEntries** . 
    
**cbEntries**
  
> Nombre d’octets dans le tableau décrit par **abEntries**. 
    
**abEntries**
  
> Tableau d’octets qui contient une ou plusieurs structures **FLATENTRY** , organisées de bout en bout. 
    
## <a name="remarks"></a>Remarques

Dans le tableau **abEntries** , chaque structure **FLATENTRY** est aligné sur une limite alignée naturellement. Octets supplémentaires sont inclus comme remplissage pour rendre l’alignement que naturel entre les deux structures **FLATENTRY** . La première structure **FLATENTRY** dans le tableau est toujours alignée correctement, car le décalage du membre **abEntries** est 8. Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée d’arrondi au multiple prochain de 4. Utilisez la macro [CbFLATENTRY](cbflatentry.md) pour calculer la taille d’une structure **FLATENTRY** . 
  
Par exemple, la deuxième structure **FLATENTRY** commence à un décalage qui comprend le décalage de la première entrée ainsi que la longueur de la première entrée d’arrondi pour les quatre octets. La longueur de la première entrée est la longueur de ses membres **cb** ainsi que la longueur de ses membres **abEntry** . 
  
L’exemple de code suivant indique comment calculer les décalages dans une structure **FLATENTRYLIST** . Supposons que _lpFlatEntry_ est un pointeur vers la première structure dans la liste. 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>Voir aussi

- [FLATENTRY](flatentry.md)
- [Propriété canonique PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)
- [Structures MAPI](mapi-structures.md)

