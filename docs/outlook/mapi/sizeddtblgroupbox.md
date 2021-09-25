---
title: SizedDtblGroupBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblGroupBox
api_type:
- COM
ms.assetid: 7ca01bf7-5185-41cc-907e-01f256345997
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1a9f5b2d26c4cfaa0232193e1a75ca3a7edca7a7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566674"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLGROUPBOX](dtblgroupbox.md) pour décrire un contrôle de zone de groupe et une étiquette d’une longueur spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLGROUPBOX** <br/> |
   
```cpp
SizedDtblGroupBox (n, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Longueur de l’étiquette de la zone de groupe. 
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblGroupBox** vous permet de définir un contrôle de zone de groupe lorsque la longueur de l’étiquette est connue. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLGROUPBOX dtblgroupbox;
TCHAR lpszLabel[n];

```

Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblGroupBox** en tant que pointeur de structure **DTBLGROUPBOX,** effectuez la distribution suivante : 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>Voir aussi

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Macros liées aux structures](macros-related-to-structures.md)

