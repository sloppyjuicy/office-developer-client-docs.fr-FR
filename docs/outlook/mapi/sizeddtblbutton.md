---
title: SizedDtblButton
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: dc4d3a7a827e728dfd6725ac269350067d4530cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590343"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLBUTTON](dtblbutton.md) pour la description d’un bouton et une étiquette d’une longueur spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>Paramètres

 _n_
  
> Longueur de l’étiquette à inclure dans la nouvelle structure.
    
 _u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La nouvelle structure est créée avec les membres suivants :
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>Voir aussi



[DTBLBUTTON](dtblbutton.md)


[Macros liées aux structures](macros-related-to-structures.md)

