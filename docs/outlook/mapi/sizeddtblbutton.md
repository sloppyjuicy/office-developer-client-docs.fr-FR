---
title: SizedDtblButton
description: Décrit SizedDtblButton, qui crée une structure nommée qui inclut une structure DTBLBUTTON pour décrire un bouton et une étiquette d’une longueur spécifiée.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblButton
api_type:
- COM
ms.assetid: ee73ced9-14d8-4a30-9b9f-d54ed9c3a454
ms.openlocfilehash: 7efb2e686835556b45e4b995f78d86c53488a8a7
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894900"
---
# <a name="sizeddtblbutton"></a>SizedDtblButton

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui [inclut une structure DTBLBUTTON](dtblbutton.md) pour décrire un bouton et une étiquette d’une longueur spécifiée. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure associée :  <br/> |**DTBLBUTTON** <br/> |
   
```cpp
SizedDtblButton (n, u)
```

## <a name="parameters"></a>Paramètres

 _n_
  
> Longueur de l’étiquette à inclure dans la nouvelle structure.
    
 _U_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La nouvelle structure est créée avec les membres suivants :
  
```
DTBLBUTTON dtblbutton;
TCHAR lpszLabel[n];

```

## <a name="see-also"></a>Voir aussi



[DTBLBUTTON](dtblbutton.md)


[Macros liées aux structures](macros-related-to-structures.md)

