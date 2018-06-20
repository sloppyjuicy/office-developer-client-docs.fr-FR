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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3de56b12fa7d34004fddbfe3633b8b8307c0ffc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787159"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**S’applique à**: Outlook 
  
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


[Macros relatives aux Structures](macros-related-to-structures.md)

