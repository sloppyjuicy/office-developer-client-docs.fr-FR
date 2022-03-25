---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: Crée une structure nommée qui inclut une structure DTBLLABEL pour décrire un contrôle d’étiquette et l’étiquette associée d’une longueur spécifiée.
ms.openlocfilehash: e286701ca57802bb8f0123321ff25da1e9cce6f3
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781333"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLLABEL](dtbllabel.md) pour décrire un contrôle d’étiquette et l’étiquette associée d’une longueur spécifiée. 
  
|Propriété |Valeur |
|:-----|:-----|
|Spécifié dans le fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
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

La macro **SizedDtblLabel** vous permet de définir une étiquette de tableau d’affichage lorsque le nombre de caractères de l’étiquette est connu. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblLabel** en tant que pointeur de structure **DTBLLABEL** , effectuez la distribution suivante : 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Voir aussi

- [DTBLLABEL](dtbllabel.md)
- [Macros liées aux structures](macros-related-to-structures.md)

