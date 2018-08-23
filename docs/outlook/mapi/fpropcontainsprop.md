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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b08d3af8c61d8ced31e822bb787d49ad90b4df54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571674"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Compare deux valeurs de propriété, généralement des chaînes ou des tableaux binaires, pour voir si un contient l’autre. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Paramètres

_lpSPropValueDst_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant la valeur de la propriété qui peut contenir la chaîne de recherche indiqué par le paramètre _lpSPropValueSrc_ . 
    
_lpSPropValueSrc_
  
> [in] Pointeur vers une structure **SPropValue** définition de la chaîne de recherche qui recherche **FPropContainsProp** dans la valeur de propriété indiqué par le paramètre _lpSPropValueDst_ . 
    
_ulFuzzyLevel_
  
> [in] Paramètres d’option définissant le niveau de précision que permettent à utiliser dans la comparaison. 

  - Les **16 bits inférieurs** s’appliquent aux propriétés de type PT_BINARY et PT_STRING8. Elles doivent être définies exactement une des valeurs suivantes :
      
    - FL_FULLSTRING : La chaîne de recherche _lpSPropValueSrc_ doit être égale à la valeur de la propriété identifiée par _lpSPropValueDst_.
        
    - FL_PREFIX : La chaîne de recherche _lpSPropValueSrc_ doit apparaître au début de la valeur de la propriété identifié par _lpSPropValueDst_. Les deux valeurs doivent être comparées uniquement jusqu'à la longueur de la chaîne de recherche indiquée par _lpSPropValueSrc_. 
        
    - FL_SUBSTRING : La chaîne de recherche _lpSPropValueSrc_ doit figurer n’importe où dans la valeur de la propriété identifiée par _lpSPropValueDst_. 
      
  - Les **derniers 16 bits** s’appliquent uniquement aux propriétés de type PT_STRING8. Elles peuvent être définies aux valeurs suivantes dans n’importe quelle combinaison :
    
    - FL_IGNORECASE : La comparaison doit être effectuée sans tenir compte de la casse. 
        
    - FL_IGNORENONSPACE : La comparaison doit ignorer Unicode définie par les caractères tels que diacritiques. 
        
    - FL_LOOSE : La comparaison doit indiquer une correspondance la mesure du possible, indépendamment de la casse sensibilité et les caractères.
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> Les paramètres sont valides et du contenu de la chaîne de recherche _lpSPropValueSrc_ comme indiqué dans la valeur de la propriété _lpSPropValueDst_ . 
    
FALSE 
  
> Les valeurs de propriété comparées ne sont pas du type PT_STRING8 ou PT_BINARY, les valeurs de propriété sont de types différents, ou la chaîne de recherche _lpSPropValueSrc_ n’est pas contenue comme indiqué dans la valeur de la propriété _lpSPropValueDst_ . 
    
## <a name="remarks"></a>Remarques

La méthode de comparaison varie selon les types de propriétés spécifiés dans les définitions de propriétés [SPropValue](spropvalue.md) et l’heuristique de niveau approximative fournies dans le paramètre _ulFuzzyLevel_ . Les fonctions [FPropCompareProp](fpropcompareprop.md) et **FPropContainsProp** peuvent servir à préparer des restrictions pour la génération d’une table. 
  
Les 16 bits de _ulFuzzyLevel_ sont ignorés pour le type de propriété PT_BINARY. Si les paramètres de _ulFuzzyLevel_ sont manquants ou non valides, une correspondance exacte de chaîne complète est effectuée. Pour plus d’informations sur la relation contenant-contenu propriété, voir la structure [SContentRestriction](scontentrestriction.md) . 
  

