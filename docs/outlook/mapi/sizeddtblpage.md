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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ae3f84c6b219c7becb88737f0d6c9fcb9722ea34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584967"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
- [Macros liées aux structures](macros-related-to-structures.md)

