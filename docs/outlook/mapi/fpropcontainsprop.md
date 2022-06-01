---
title: FPropContainsProp
description: Décrit FPropContainsProp et fournit la syntaxe, les paramètres et la valeur de retour.
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
ms.openlocfilehash: de9b2930b714a33e88591c3e99bff1b049decb92
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817738"
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
  
> [in] Pointeur vers une structure **SPropValue** définissant la chaîne de recherche recherchée par **FPropContainsProp** dans la valeur de propriété pointée par le paramètre  _lpSPropValueDst_ . 
    
_ulFuzzyLevel_
  
> [in] Paramètres d’option définissant le niveau de précision à utiliser dans la comparaison. 

  - Les **16 bits inférieurs** s’appliquent aux propriétés de type PT_BINARY et PT_STRING8. Elles doivent être définies sur exactement l’une des valeurs suivantes :
      
    - FL_FULLSTRING : la chaîne de recherche  _lpSPropValueSrc_ doit être égale à la valeur de propriété identifiée par  _lpSPropValueDst_.
        
    - FL_PREFIX : la chaîne de recherche  _lpSPropValueSrc_ doit apparaître au début de la valeur de propriété identifiée par  _lpSPropValueDst_. Les deux valeurs doivent être comparées uniquement jusqu’à la longueur de la chaîne de recherche indiquée par  _lpSPropValueSrc_. 
        
    - FL_SUBSTRING : la chaîne de recherche  _lpSPropValueSrc_ doit être contenue n’importe où dans la valeur de propriété identifiée par  _lpSPropValueDst_. 
      
  - Les **16 bits supérieurs** s’appliquent uniquement aux propriétés de type PT_STRING8. Elles peuvent être définies sur les valeurs suivantes dans n’importe quelle combinaison :
    
    - FL_IGNORECASE : La comparaison doit être effectuée sans tenir compte de la sensibilité de la casse. 
        
    - FL_IGNORENONSPACE : la comparaison doit ignorer les caractères d’espacement non définis par Unicode, tels que les marques diacritiques. 
        
    - FL_LOOSE : la comparaison doit indiquer une correspondance dans la mesure du possible, en ignorant la sensibilité de la casse et les caractères d’espacement.
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Les paramètres sont tous valides et la chaîne de recherche  _lpSPropValueSrc_ est contenue comme spécifié dans la valeur de propriété _lpSPropValueDst_ . 
    
FALSE 
  
> Les valeurs de propriété comparées ne sont pas de type PT_STRING8 ou PT_BINARY, les valeurs de propriété sont de types différents ou la chaîne de recherche  _lpSPropValueSrc_ n’est pas contenue comme spécifié dans la valeur de propriété _lpSPropValueDst_ . 
    
## <a name="remarks"></a>Remarques

La méthode de comparaison dépend des types de propriétés spécifiés dans les définitions de [propriétés SPropValue](spropvalue.md) et du niveau approximative heuristique fourni dans le paramètre _ulFuzzyLevel_ . Les fonctions [FPropCompareProp](fpropcompareprop.md) et **FPropContainsProp peuvent être utilisées** pour préparer des restrictions pour la génération d’une table. 
  
Les 16 bits supérieurs  _d’ulFuzzyLevel_ sont ignorés pour le type de propriété PT_BINARY. Si les paramètres dans  _ulFuzzyLevel_ sont manquants ou non valides, une correspondance exacte de chaîne complète est effectuée. Pour plus d’informations sur l’endiguement des propriétés, consultez la structure [SContentRestriction](scontentrestriction.md) . 
  

