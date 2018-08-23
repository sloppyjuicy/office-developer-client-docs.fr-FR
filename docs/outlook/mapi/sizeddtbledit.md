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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7e50589b52f3e99bf2569a55bb7d3ca4f8247fd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591659"
---
# <a name="sizeddtbledit"></a>SizedDtblEdit

**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
- [Macros liées aux structures](macros-related-to-structures.md)

