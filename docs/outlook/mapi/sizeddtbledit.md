---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 22ff75605b9ab7911f0a270a17631f8261b54ffc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566681"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLEDIT](dtbledit.md) pour décrire un contrôle d’édition et le nombre maximal de caractères qui peuvent être entrés dans le contrôle. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLEDIT** <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Nombre maximal de caractères qui peuvent être entrés dans le contrôle d’édition.
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblEdit** vous permet de définir un contrôle d’édition lorsque le nombre de caractères activés est connu. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblEdit** en tant que pointeur de structure **DTBLEDIT,** effectuez la distribution suivante : 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Voir aussi

- [DTBLEDIT](dtbledit.md)
- [Macros liées aux structures](macros-related-to-structures.md)

