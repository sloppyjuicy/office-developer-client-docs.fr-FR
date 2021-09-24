---
title: SExistRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SExistRestriction
api_type:
- COM
ms.assetid: 48d5ab42-ee70-4f6e-9184-18d22b08ea1b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8e2cf26b2e4388fac1432308df82ded911cf7501
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550035"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une restriction existante utilisée pour tester si une propriété particulière existe en tant que colonne dans le tableau. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
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
  
> Réservé ; doit être zéro. 
    
 **ulPropTag**
  
> Balise de propriété identifiant la colonne à tester pour l’existence dans chaque ligne.
    
 **ulReserved2**
  
> Réservé ; doit être zéro.
    
## <a name="remarks"></a>Remarques

La restriction existante est utilisée pour garantir des résultats significatifs pour d’autres types de restrictions qui impliquent des propriétés, telles que les restrictions de propriété et de contenu. Lorsqu’une restriction qui implique une propriété est transmise à [IMAPITable::Restrict](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md) et que la propriété n’existe pas, les résultats de la restriction ne sont pas indéfinis. En créant une restriction **AND** qui joint la restriction de propriété à une restriction existante, un appelant peut obtenir des résultats précis. 
  
Les restrictions existantes ne peuvent pas être utilisées avec les propriétés de sous-objet qui ont des PT_OBJECT. 
  
Pour plus d’informations sur la structure **SExistRestriction,** voir [À propos des restrictions.](about-restrictions.md) 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

