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
ms.openlocfilehash: 7433342fb74ff09d5ec427aa457deb8c753da16d
ms.sourcegitcommit: a1434c24ee2b92bd0faac5f37d9baa1d05b42058
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/27/2022
ms.locfileid: "67052442"
---
# <a name="sizeddtbllabel"></a>SizedDtblLabel

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui [inclut une structure DTBLLABEL](dtbllabel.md) pour décrire un contrôle d’étiquette et l’étiquette associée d’une longueur spécifiée. 
  
|Propriété |Valeur |
|:-----|:-----|
|Spécifié dans le fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure associée  <br/> |**DTBLLABEL** <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Longueur de l’étiquette. Cela inclut le caractère null de fin. 
    
_U_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblLabel** vous permet de définir une étiquette de table d’affichage lorsque le nombre de caractères dans l’étiquette est connu. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblLabel** en tant que pointeur de structure **DTBLLABEL** , effectuez le cast suivant : 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a>Voir aussi

- [DTBLLABEL](dtbllabel.md)
- [Macros liées aux structures](macros-related-to-structures.md)

