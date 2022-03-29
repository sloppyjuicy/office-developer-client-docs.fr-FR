---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: Crée une structure nommée qui inclut DTBLPAGE pour décrire un contrôle de page à onglets, une étiquette et une entrée de fichier d’aide d’une longueur spécifiée.
ms.openlocfilehash: 455275ca2115b06e2dfa610ad670bb31d6c50de4
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455229"
---
# <a name="sizeddtblpage"></a>SizedDtblPage

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure nommée qui inclut une structure [DTBLPAGE](dtblpage.md) pour décrire un contrôle de page à onglets, une étiquette d’une longueur spécifiée et une entrée de fichier d’aide d’une longueur spécifiée. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**DTBLPAGE** <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a>Paramètres

_n_
  
> Longueur de l’étiquette de l’onglet de page.
    
_n1_
  
> Longueur de l’entrée apparaissant dans le fichier Mapisvc.inf identifiant le fichier d’aide qui sera utilisé avec le contrôle de page à onglets.
    
_u_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

La macro **SizedDtblPage** vous permet de définir un contrôle de page à onglets lorsque le nombre de caractères dans l’étiquette associée et l’entrée du fichier d’aide sont connus. La nouvelle structure est créée avec les membres suivants : 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

Pour utiliser un pointeur vers la structure résultante de la macro **SizedDtblPage** en tant que pointeur de structure **DTBLPAGE** , effectuez la distribution suivante : 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a>Voir aussi

- [DTBLPAGE](dtblpage.md)
- [Macros liées aux structures](macros-related-to-structures.md)

