---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: Crée une structure nommée qui inclut DTBLCOMBOBOX en tant que contrôle de zone de liste déroulante et le nombre maximal de caractères qui peuvent être entrés dans le contrôle d’édition.
ms.openlocfilehash: ee3a6bdb86e7be89d3ac79d2dfb855df69491b00
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455026"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLCOMBOBOX](dtblcombobox.md) pour décrire un contrôle de zone de liste déroulante et le nombre maximal de caractères qui peuvent être entrés dans le contrôle d’édition associé. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Nombre de caractères qui peuvent être entrés dans le contrôle d’édition de la zone de liste modifiable. 
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblComboBox** vous permet de définir une zone de liste déroulante lorsque la longueur de la chaîne de caractères activée est connue. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblComboBox** en tant que pointeur de structure **DTBLCOMBOBOX** , effectuez la distribution suivante : 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>Voir aussi

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Macros liées aux structures](macros-related-to-structures.md)

