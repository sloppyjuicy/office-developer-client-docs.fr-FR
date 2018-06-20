---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c2e275e373677e50510a0aa87f5060070a870a0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787183"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**S’applique à**: Outlook 
  
Crée une structure nommée qui inclut une structure [DTBLLABEL](dtbllabel.md) pour la description d’un contrôle label et l’étiquette associé d’une longueur spécifiée. 
  
|||
|:-----|:-----|
|Spécifié dans le fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Longueur de l’étiquette. Cela inclut le caractère NULL de fin. 
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblLabel** vous permet de définir une étiquette d’affichage tableau lorsque le nombre de caractères dans l’étiquette est connu. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblLabel** comme un pointeur de structure **DTBLLABEL** , effectuer le cast suivant : 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Voir aussi

- [DTBLLABEL](dtbllabel.md)
- [Macros relatives aux Structures](macros-related-to-structures.md)

