---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6e3cdcf3579b26776d9e278bb339758d4f56d890
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339276"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction existante qui est utilisée pour tester si une propriété particulière existe sous forme de colonne dans le tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SExistRestriction
{
  ULONG ulReserved1;
  ULONG ulPropTag;
  ULONG ulReserved2;
} SExistRestriction;

```

## <a name="members"></a>Members

 **ulReserved1**
  
> MSR doit être égal à zéro. 
    
 **ulPropTag**
  
> Balise de propriété identifiant la colonne devant être testée pour chaque ligne.
    
 **ulReserved2**
  
> MSR doit être égal à zéro.
    
## <a name="remarks"></a>Remarques

La restriction EXISTS est utilisée pour garantir des résultats significatifs pour d'autres types de restrictions qui impliquent des propriétés, telles que les restrictions de propriété et de contenu. Lorsqu'une restriction impliquant une propriété est transmise à une propriété [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md) et que la propriété n'existe pas, les résultats de la restriction ne sont pas définis. En créant une restriction **et** qui rejoint la restriction de propriété avec une restriction existante, un appelant peut être assuré de résultats précis. 
  
Les restrictions d'existence ne peuvent pas être utilisées avec des propriétés de sous-objet de type PT_OBJECT. 
  
Pour plus d'informations sur la structure **SExistRestriction** , consultez la rubrique [à propos des restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

