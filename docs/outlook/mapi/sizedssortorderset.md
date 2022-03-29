---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: Crée une structure SSortOrderSet nommée qui contient un nombre spécifié d’ordres de tri pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: d8cdc5ffc5194f70ace85f8dbcc51afaa77c1804
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454704"
---
# <a name="sizedssortorderset"></a>SizedSSortOrderSet

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée une structure [SSortOrderSet nommée](ssortorderset.md) qui contient un nombre spécifié d’ordres de tri. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Structure connexe :  <br/> |**SSortOrderSet** <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a>Paramètres

_ _csort_
  
> Nombre d’ordres de tri à inclure dans la nouvelle structure.
    
_ _name_
  
> Nom de la nouvelle structure.
    
## <a name="remarks"></a>Remarques

Utilisez la macro **SizedSSortOrderSet** pour créer un ordre de tri avec des limites explicites. 
  
Pour utiliser la nouvelle structure qui résulte de la macro **SizedSSortOrderSet** comme pointeur vers une structure **SSortOrderSet** , effectuez la distribution suivante : 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a>Voir aussi

- [SSortOrderSet](ssortorderset.md)
- [Macros liées aux structures](macros-related-to-structures.md)

