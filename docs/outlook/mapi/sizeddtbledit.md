---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4ea77023bdc9442325f4af46d23c107e7172ceaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787166"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**S’applique à**: Outlook 
  
Crée une structure nommée qui inclut une structure [DTBLEDIT](dtbledit.md) pour la description d’un contrôle d’édition et le nombre maximal de caractères pouvant être entré dans le contrôle. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Nombre maximal de caractères pouvant être entré dans le contrôle d’édition.
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblEdit** vous permet de définir un contrôle d’édition lorsque le nombre de caractères activés est connu. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblEdit** comme un pointeur de structure **DTBLEDIT** , effectuer le cast suivant : 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Voir aussi

- [DTBLEDIT](dtbledit.md)
- [Macros relatives aux Structures](macros-related-to-structures.md)

