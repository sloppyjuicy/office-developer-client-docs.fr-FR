---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432630"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux valeurs de propriété, généralement des chaînes ou des tableaux binaires, pour voir si l’une contient l’autre. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Parameters

_lpSPropValueDst_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant la valeur de propriété qui peut contenir la chaîne de recherche pointée par le paramètre _lpSPropValueSrc._ 
    
_lpSPropValueSrc_
  
> [in] Pointeur vers une structure **SPropValue** définissant la chaîne de recherche que **FPropContainsProp** recherche dans la valeur de propriété pointée par le paramètre _lpSPropValueDst._ 
    
_ulFuzzyLevel_
  
> [in] Paramètres d’option définissant le niveau de précision à utiliser dans la comparaison. 

  - Les **16 bits inférieurs** s’appliquent aux propriétés de type PT_BINARY et PT_STRING8. Elles doivent être définies sur l’une des valeurs suivantes :
      
    - FL_FULLSTRING : la chaîne de recherche  _lpSPropValueSrc_ doit être égale à la valeur de propriété identifiée par  _lpSPropValueDst_.
        
    - FL_PREFIX : la chaîne de recherche  _lpSPropValueSrc_ doit apparaître au début de la valeur de propriété identifiée par  _lpSPropValueDst_. Les deux valeurs doivent être comparées uniquement jusqu’à la longueur de la chaîne de recherche indiquée par  _lpSPropValueSrc_. 
        
    - FL_SUBSTRING : la chaîne de recherche  _lpSPropValueSrc_ doit être contenue n’importe où dans la valeur de propriété identifiée par  _lpSPropValueDst_. 
      
  - Les **16 bits supérieurs** s’appliquent uniquement aux propriétés de type PT_STRING8. Elles peuvent être définies sur les valeurs suivantes dans n’importe quelle combinaison :
    
    - FL_IGNORECASE : la comparaison doit être réalisée sans tenir compte de la sensibilité à la cas. 
        
    - FL_IGNORENONSPACE : la comparaison doit ignorer les caractères non définis par Unicode, tels que les signes diacritiques. 
        
    - FL_LOOSE : la comparaison doit indiquer une correspondance dans la mesure du possible, en ignorant les caractères de respect de la cas et d’espacement.
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Les paramètres sont tous valides et la chaîne de recherche _lpSPropValueSrc_ est contenue comme spécifié dans la valeur de la propriété _lpSPropValueDst._ 
    
FALSE 
  
> Les valeurs de propriété comparées ne sont pas de type PT_STRING8 ou PT_BINARY, les valeurs de propriété sont de types différents ou la chaîne de recherche _lpSPropValueSrc_ n’est pas contenue comme spécifié dans la valeur de la propriété _lpSPropValueDst._ 
    
## <a name="remarks"></a>Remarques

La méthode de comparaison dépend des types de propriétés spécifiés dans les définitions de [propriétés SPropValue](spropvalue.md) et de l’heuristique de niveau fuzzy fourni dans le paramètre _ulFuzzyLevel._ Les [fonctions FPropCompareProp](fpropcompareprop.md) et **FPropContainsProp** peuvent être utilisées pour préparer les restrictions de génération d’une table. 
  
Les 16 bits supérieurs de  _ulFuzzyLevel_ sont ignorés pour le type de PT_BINARY. Si les paramètres de  _ulFuzzyLevel_ sont manquants ou non valides, une correspondance exacte de chaîne complète est effectuée. Pour plus d’informations sur le contenu des propriétés, voir la structure [SContentRestriction.](scontentrestriction.md) 
  

