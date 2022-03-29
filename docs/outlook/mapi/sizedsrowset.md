---
title: SizedSRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedSRowSet
api_type:
- COM
ms.assetid: 419e2c6d-ac3b-46c6-9a12-33f51f6d7f12
description: Crée une structure SRowSet nommée qui contient un nombre spécifié de lignes pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: b2aea56f39eee8d37b565efc38db70e7b248c85a
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456272"
---
# <a name="sizedsrowset"></a>SizedSRowSet

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure [SRowSet nommée](srowset.md) qui contient un nombre spécifié de lignes. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**SRowSet** <br/> |
   
```cpp
SizedSRowSet (_crow, _name)
```

## <a name="parameters"></a>Paramètres

_ _sous_
  
> Nombre de lignes à inclure dans la nouvelle structure.
    
_ _name_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Pour utiliser la nouvelle structure qui résulte de la macro **SizedSRowSet** comme pointeur vers une structure **SRowSet** , effectuez la distribution suivante : 
  
```cpp
lpSRowSet = (LPSRowSet) &SizedSRowSet;

```

## <a name="see-also"></a>Voir aussi

- [SRowSet](srowset.md)
- [Macros liées aux structures](macros-related-to-structures.md)

