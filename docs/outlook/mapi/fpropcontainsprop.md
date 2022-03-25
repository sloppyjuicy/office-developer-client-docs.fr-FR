---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a8c5ef13513e12776a787890c23fd766ce60e7b9
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63783426"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux valeurs de propriété, généralement des chaînes ou des tableaux binaires, pour voir si l’une contient l’autre. 
  
|Propriété|Valeur|
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

## <a name="parameters"></a>Paramètres

_lpSPropValueDst_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant la valeur de propriété qui peut contenir la chaîne de recherche pointée par le paramètre  _lpSPropValueSrc_ . 
    
_lpSPropValueSrc_
  
> [in] Pointeur vers une structure **SPropValue** définissant la chaîne de recherche que **FPropContainsProp** recherche dans la valeur de propriété pointée par le paramètre  _lpSPropValueDst_ . 
    
_ulFuzzyLevel_
  
> [in] Paramètres d’option définissant le niveau de précision à utiliser dans la comparaison. 

  - Les **16 bits inférieurs s’appliquent aux propriétés** de type PT_BINARY et PT_STRING8. Elles doivent être définies sur l’une des valeurs suivantes :
      
    - FL_FULLSTRING : la chaîne de recherche  _lpSPropValueSrc_ doit être égale à la valeur de propriété identifiée par  _lpSPropValueDst_.
        
    - FL_PREFIX : la chaîne de recherche  _lpSPropValueSrc_ doit apparaître au début de la valeur de propriété identifiée par  _lpSPropValueDst_. Les deux valeurs doivent être comparées uniquement jusqu’à la longueur de la chaîne de recherche indiquée par  _lpSPropValueSrc_. 
        
    - FL_SUBSTRING : la chaîne de recherche  _lpSPropValueSrc_ doit être contenue n’importe où dans la valeur de propriété identifiée par  _lpSPropValueDst_. 
      
  - Les **16 bits supérieurs s’appliquent uniquement aux propriétés** de type PT_STRING8. Elles peuvent être définies sur les valeurs suivantes dans n’importe quelle combinaison :
    
    - FL_IGNORECASE : la comparaison doit être réalisée sans tenir compte de la sensibilité à la cas. 
        
    - FL_IGNORENONSPACE : la comparaison doit ignorer les caractères non définis par Unicode, tels que les signes diacritiques. 
        
    - FL_LOOSE : la comparaison doit indiquer une correspondance chaque fois que possible, en ignorant la sensibilité de la cas et les caractères non espacement.
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Les paramètres sont tous valides et la chaîne de recherche  _lpSPropValueSrc_ est contenue comme spécifié dans la valeur de la propriété _lpSPropValueDst_ . 
    
FALSE 
  
> Les valeurs de propriété comparées ne sont pas de type PT_STRING8 ou PT_BINARY, les valeurs de propriété sont de types différents ou la chaîne de recherche  _lpSPropValueSrc_ n’est pas contenue comme spécifié dans la valeur de la propriété _lpSPropValueDst_ . 
    
## <a name="remarks"></a>Remarques

La méthode de comparaison dépend des types de propriétés spécifiés dans les définitions de [propriétés SPropValue](spropvalue.md) et de l’heuristique de niveau fuzzy fourni dans le paramètre _ulFuzzyLevel_ . Les [fonctions FPropCompareProp](fpropcompareprop.md) et **FPropContainsProp** peuvent être utilisées pour préparer les restrictions de génération d’une table. 
  
Les 16 bits supérieurs de  _ulFuzzyLevel_ sont ignorés pour le type de PT_BINARY. Si les paramètres de  _ulFuzzyLevel_ sont manquants ou non valides, une correspondance exacte de chaîne complète est effectuée. Pour plus d’informations sur le contenu des propriétés, voir [la structure SContentRestriction](scontentrestriction.md) . 
  

