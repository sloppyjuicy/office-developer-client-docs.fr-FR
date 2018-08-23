---
title: SizedDtblCheckBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblCheckBox
api_type:
- COM
ms.assetid: 9d04a124-54d4-43ac-967f-ea8e7a09b1d0
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6120439ea0d98ed6b64fe1542a4372265574723a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567530"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLCHECKBOX](dtblcheckbox.md) pour la description d’un contrôle de case à cocher et une étiquette d’une longueur spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLCHECKBOX** <br/> |
   
```cpp
SizedDtblCheckBox (n, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Longueur de l’étiquette à inclure dans la nouvelle structure.
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblCheckBox** vous permet de définir une case à cocher lorsque le nombre de caractères de l’étiquette est connu. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLCHECKBOX dtblcheckbox;
TCHAR lpszLabel[n];
```

Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblCheckBox** comme un pointeur de structure **DTBLCHECKBOX** , effectuer le cast suivant : 
  
```cpp
lpDtblCheckBox = (LPDTBLCHECKBOX) &SizedDtblCheckBox;
```

## <a name="see-also"></a>Voir aussi

- [DTBLCHECKBOX](dtblcheckbox.md)
- [Macros liées aux structures](macros-related-to-structures.md)

