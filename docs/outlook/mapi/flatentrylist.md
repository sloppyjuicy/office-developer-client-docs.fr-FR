---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: Contient un tableau de structures FLATENTRY.
ms.openlocfilehash: dfe499a8e7432f1bbd6c3acd2ef6b84d586d5592
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558767"
---
# <a name="flatentrylist"></a>FLATENTRYLIST

**S’applique à** : Outlook 2013 | Outlook 2016
  
Contient un tableau de structures [FLATENTRY](flatentry.md) .
  
|**Informations**|**Valeur**|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros associées :  <br/> |[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md) <br/> |

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
  
> Nombre de structures **FLATENTRY** dans le tableau décrit par le **membre abEntries** .

**cbEntries**
  
> Nombre d’octets dans le tableau décrit par **abEntries**.

**abEntries**
  
> Tableau d’bytes qui contient une ou plusieurs structures **FLATENTRY** , organisées de bout en bout.

## <a name="remarks"></a>Remarques

Dans le **tableau abEntries** , chaque structure **FLATENTRY** est alignée sur une limite alignée naturellement. Des octets supplémentaires sont inclus comme remplissage pour assurer un alignement naturel entre deux structures **FLATENTRY** . La première structure **FLATENTRY** du tableau est toujours alignée correctement, car le décalage du membre **abEntries** est 8. Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée arrondie au multiple suivant de 4. Utilisez la macro [CbFLATENTRY](cbflatentry.md) pour calculer la taille d’une structure **FLATENTRY** .
  
Par exemple, la deuxième structure **FLATENTRY** commence par un décalage qui se compose du décalage de la première entrée plus la longueur de la première entrée arrondie aux quatre octets suivants. La longueur de la première entrée est la longueur de son membre **cb** ainsi que la longueur de son **membre abEntry** .
  
L’exemple de code suivant indique comment calculer des décalages dans une structure **FLATENTRYLIST** . Supposons _que lpFlatEntry_ est un pointeur vers la première structure de la liste.
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a>Voir aussi

- [FLATENTRY](flatentry.md)
- [Propriété canonique PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)
- [Structures MAPI](mapi-structures.md)
