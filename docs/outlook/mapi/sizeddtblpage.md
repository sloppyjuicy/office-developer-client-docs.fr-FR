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
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282656"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLPAGE](dtblpage.md) pour la description d'un contrôle de page à onglets, une étiquette d'une longueur spécifiée et une entrée de fichier d'aide d'une longueur spécifiée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Structure associée:  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Longueur de l'étiquette de l'onglet de page.
    
_N1_
  
> Longueur de l'entrée apparaissant dans le fichier MAPISVC. inf identifiant le fichier d'aide qui sera utilisé avec le contrôle de page à onglets.
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblPage** vous permet de définir un contrôle de page à onglets lorsque le nombre de caractères dans l'étiquette associée et l'entrée de fichier d'aide est connu. La nouvelle structure est créée avec les membres suivants: 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Pour utiliser un pointeur vers la structure obtenue à partir de la macro **SizedDtblPage** en tant que pointeur de structure **DTBLPAGE** , effectuez la conversion suivante: 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>Voir aussi

- [DTBLPAGE](dtblpage.md)
- [Macros liées aux structures](macros-related-to-structures.md)

