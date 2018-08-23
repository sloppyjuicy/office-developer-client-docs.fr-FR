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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 39854c320078d2e2ca2365244f094e28962380d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593654"
---
# <a name="sizeddtblcombobox"></a>SizedDtblComboBox
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
- [Macros liées aux structures](macros-related-to-structures.md)

