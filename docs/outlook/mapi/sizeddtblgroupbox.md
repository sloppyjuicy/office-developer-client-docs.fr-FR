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
description: Crée une structure nommée qui inclut une structure DTBLGROUPBOX pour décrire un contrôle de zone de groupe et une étiquette d’une longueur spécifiée.
ms.openlocfilehash: ca66c050b7be7846178da49fd3912ce51433ea6e
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455236"
---
# <a name="sizeddtblgroupbox"></a>SizedDtblGroupBox

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLGROUPBOX](dtblgroupbox.md) pour décrire un contrôle de zone de groupe et une étiquette d’une longueur spécifiée. 
  
|Propriété |Valeur |
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

Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblGroupBox** en tant que pointeur de structure **DTBLGROUPBOX** , effectuez la distribution suivante : 
  
```cpp
lpDtblGroupBox = (LPDTBLGROUPBOX) &SizedDtblGroupBox;

```

## <a name="see-also"></a>Voir aussi

- [DTBLGROUPBOX](dtblgroupbox.md)
- [Macros liées aux structures](macros-related-to-structures.md)

