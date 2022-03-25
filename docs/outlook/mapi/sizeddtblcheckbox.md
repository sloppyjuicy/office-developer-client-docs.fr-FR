---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: Crée une structure nommée qui inclut une structure DTBLCHECKBOX pour décrire un contrôle case à cocher et une étiquette d’une longueur spécifiée.
ms.openlocfilehash: 14b2de2030a1f23765bab157932543d249a88824
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405278"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLCHECKBOX](dtblcheckbox.md) pour décrire un contrôle case à cocher et une étiquette d’une longueur spécifiée. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Longueur de l’étiquette à inclure dans la nouvelle structure.
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblCheckBox** vous permet de définir une case à cocher lorsque le nombre de caractères d’étiquette est connu. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblCheckBox** en tant que pointeur de structure **DTBLCHECKBOX** , effectuez la distribution suivante : 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>Voir aussi

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Macros liées aux structures](macros-related-to-structures.md)

