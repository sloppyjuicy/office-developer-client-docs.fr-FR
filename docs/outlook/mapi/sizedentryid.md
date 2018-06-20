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
ms.openlocfilehash: 814cfeab61854469f460cc38f927b0e3723f6f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787172"
---
# <a name="sizedentryid"></a>SizedENTRYID

**S’applique à**: Outlook 
  
Crée une structure [ENTRYID](entryid.md) nommée qui contient un membre de **Carnet d’adresses** d’une taille spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**PROPRIÉTÉ ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Paramètres

__cb_
  
> Nombre d’octets dans le membre de **Carnet d’adresses** de la nouvelle structure. 
    
__nom_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedENTRYID** vous permet de définir un identificateur d’entrée une fois que les besoins en matière de longueur de tableau. Utilisez cette macro pour créer un identificateur d’entrée avec des limites explicites. 
  
Pour utiliser la nouvelle structure de résultats de la macro **SizedENTRYID** comme un pointeur vers une structure **ENTRYID** , effectuer le cast suivant : 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Voir aussi

- [PROPRIÉTÉ ENTRYID](entryid.md)
- [Macros relatives aux Structures](macros-related-to-structures.md)

