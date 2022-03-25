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
description: Crée une structure nommée qui inclut une structure DTBLEDIT pour décrire un contrôle d’édition et le nombre de caractères qui peuvent être entrés dans le contrôle.
ms.openlocfilehash: 38ced2bfd3b08104c49c91d170425749e3a8ad08
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64406364"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLEDIT](dtbledit.md) pour décrire un contrôle d’édition et le nombre maximal de caractères qui peuvent être entrés dans le contrôle. 
  
|Propriété |Valeur |
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

Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblEdit** en tant que pointeur de structure **DTBLEDIT** , effectuez la distribution suivante : 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a>Voir aussi

- [DTBLEDIT](dtbledit.md)
- [Macros liées aux structures](macros-related-to-structures.md)

