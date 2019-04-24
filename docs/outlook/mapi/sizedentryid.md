---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282683"
---
# <a name="sizedentryid"></a>SizedENTRYID

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure [EntryID](entryid.md) nommée qui contient un membre **AB** d'une taille spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Structure associée:  <br/> |**ENTRÉE** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Paramètres

__CB_
  
> Nombre d'octets dans le membre **AB** de la nouvelle structure. 
    
__nom_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedENTRYID** vous permet de définir un identificateur d'entrée après des exigences de longueur de tableau connues. Utilisez cette macro pour créer un identificateur d'entrée avec des limites explicites. 
  
Pour utiliser la nouvelle structure qui résulte de la macro **SizedENTRYID** en tant que pointeur vers une structure **EntryID** , effectuez la conversion suivante: 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Voir aussi

- [ENTRÉE](entryid.md)
- [Macros liées aux structures](macros-related-to-structures.md)

