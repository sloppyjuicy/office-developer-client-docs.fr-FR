---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a1530443600df7cb73ff27d5cfbeab46f81bc53c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787169"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**S’applique à**: Outlook 
  
Crée une structure nommée qui inclut une structure [DTBLPAGE](dtblpage.md) pour la description d’un contrôle de la page à onglets, une étiquette d’une longueur spécifiée, une entrée de fichier d’aide d’une longueur spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Longueur de l’étiquette de l’onglet page.
    
_N1_
  
> Longueur de l’entrée figurant dans le fichier Mapisvc.inf qui identifie le fichier d’aide qui sera utilisé avec le contrôle de la page à onglets.
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblPage** vous permet de définir un contrôle de la page à onglets lorsque le nombre de caractères dans l’étiquette associée et l’entrée de fichier d’aide est connu. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblPage** comme un pointeur de structure **DTBLPAGE** , effectuer le cast suivant : 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>Voir aussi

- [DTBLPAGE](dtblpage.md)
- [Macros relatives aux Structures](macros-related-to-structures.md)

