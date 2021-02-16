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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 88cf91330dea82dda490b81cc8de6fea0504baf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405708"
---
# <a name="sizedentryid"></a>SizedENTRYID

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure [ENTRYID](entryid.md) nommée qui contient un membre **ab** d’une taille spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Paramètres

_ _cb_
  
> Nombre d’octets dans le **membre ab** de la nouvelle structure. 
    
_ _name_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedENTRYID** vous permet de définir un identificateur d’entrée une fois que les exigences de longueur du tableau sont connues. Utilisez cette macro pour créer un identificateur d’entrée avec des limites explicites. 
  
Pour utiliser la nouvelle structure qui résulte de la macro **SizedENTRYID** comme pointeur vers une structure **ENTRYID,** effectuez la distribution suivante : 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Voir aussi

- [ENTRYID](entryid.md)
- [Macros liées aux structures](macros-related-to-structures.md)

