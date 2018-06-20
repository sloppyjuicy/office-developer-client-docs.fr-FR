---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fea2b496a34d7aa7f9469158fae14daf6a770608
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787178"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**S’applique à**: Outlook 
  
Crée une structure nommée qui inclut une structure [DTBLCOMBOBOX](dtblcombobox.md) pour la description d’un contrôle de zone de liste déroulante et le nombre maximal de caractères pouvant être entré dans le contrôle d’édition associé. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLCOMBOBOX** <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Nombre de caractères pouvant figurer dans la liste déroulante du contrôle d’édition. 
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblComboBox** vous permet de définir une zone de liste déroulante lorsque la longueur de la chaîne de caractères activé est connue. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblComboBox** comme un pointeur de structure **DTBLCOMBOBOX** , effectuer le cast suivant : 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a>Voir aussi

- [DTBLCOMBOBOX](dtblcombobox.md)
- [Macros relatives aux Structures](macros-related-to-structures.md)

