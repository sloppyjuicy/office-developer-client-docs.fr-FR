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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9a30554253bc11c8905273079429e4b41c20583a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787161"
---
# <a name="sizeddtblcheckbox"></a>SizedDtblCheckBox
 
**S’applique à**: Outlook 
  
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
- [Macros relatives aux Structures](macros-related-to-structures.md)

