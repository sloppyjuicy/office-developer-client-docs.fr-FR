---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a3d8a76905aa9abb0e5bf001688608e03446704a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787174"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**S’applique à**: Outlook 
  
Crée une structure nommée qui inclut une structure [DTBLGROUPBOX](dtblgroupbox.md) pour la description d’un contrôle de zone de groupe et l’étiquette d’une longueur spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Longueur de l’étiquette de la zone de groupe. 
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblGroupBox** vous permet de définir un contrôle de zone de groupe, lorsque la longueur de l’étiquette est connue. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblGroupBox** comme un pointeur de structure **DTBLGROUPBOX** , effectuer le cast suivant : 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>Voir aussi

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Macros relatives aux Structures](macros-related-to-structures.md)

