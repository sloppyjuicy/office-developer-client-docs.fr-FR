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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 218238bea277a2d57c77fcc9d71cd622f7da42fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571947"
---
# <a name="sexistrestriction"></a>SExistRestriction

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une restriction existent qui est utilisée pour déterminer si une propriété particulière existe en tant que colonne dans le tableau. 
  
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
  
> Réservé ; doit être égal à zéro. 
    
 **ulPropTag**
  
> Balise de propriété qui identifie la colonne à tester l’existence de chaque ligne.
    
 **ulReserved2**
  
> Réservé ; doit être égal à zéro.
    
## <a name="remarks"></a>Remarques

La restriction existent est utilisée pour garantir des résultats pertinents pour les autres types de restrictions qui impliquent des propriétés, telles que des restrictions de propriété et de contenu. Lorsqu’une restriction qui implique une propriété est transmise à [IMAPITable](imapitable-restrict.md) ou [IMAPITable::FindRow](imapitable-findrow.md) et la propriété n’existe pas, les résultats de la restriction ne sont pas définis. En créant une restriction **et** qui rejoint la restriction de propriété avec une restriction existe, l’appelant peut être garanti des résultats précis. 
  
Il existe restrictions ne peut être utilisées avec les propriétés d’objet sous-sites dont type PT_OBJECT. 
  
Pour plus d’informations sur la structure **SExistRestriction** , voir [à propos des Restrictions](about-restrictions.md). 
  
## <a name="see-also"></a>Voir aussi



[SRestriction](srestriction.md)


[Structures MAPI](mapi-structures.md)

