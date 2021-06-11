---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414612"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux valeurs de propriété pour déterminer si elles sont égales. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Parameters

 _lpSPropValueA_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant la première valeur de propriété à comparer. 
    
 _lpSPropValueB_
  
> [in] Pointeur vers une structure **SPropValue** définissant la deuxième valeur de propriété à comparer. 
    
## <a name="return-value"></a>Valeur renvoyée

 **LPropCompareProp renvoie l’une** des valeurs suivantes pour la plupart des types de propriétés : 
  
- Inférieur à zéro si la valeur indiquée par le paramètre _lpSPropValueA_ est inférieure à celle indiquée par le paramètre _lpSPropValueB._ 
    
- Supérieur à zéro si la valeur indiquée par  _lpSPropValueA_ est supérieure à celle indiquée par  _lpSPropValueB_.
    
- Zéro si la valeur indiquée par  _lpSPropValueA_ est égale à la valeur indiquée par  _lpSPropValueB_. 
    
Pour les types de propriétés qui n’ont aucun ordre intrinsèque, comme les types booléens ou d’erreur, la fonction **LPropCompareProp** renvoie une valeur non définie si les deux valeurs de propriété ne sont pas égales. Cette valeur non définie est non zéro et cohérente entre les appels. 
  
## <a name="remarks"></a>Remarques

Utilisez la **fonction LPropCompareProp** uniquement si les types des deux propriétés à comparer sont identiques. 
  
Avant **d’appeler LPropCompareProp,** une application cliente ou un fournisseur de services doit d’abord récupérer les propriétés à des fins de comparaison avec un appel à la méthode [IMAPIProp::GetProps.](imapiprop-getprops.md) Lorsqu’un client ou un fournisseur appelle **LPropCompareProp,** la fonction examine d’abord les balises de propriété pour s’assurer que la comparaison des valeurs de propriété est valide. La fonction compare ensuite les valeurs des propriétés, en renvoyant une valeur appropriée. 
  
Si les valeurs de propriété sont différentes, **LPropCompareProp** détermine celle qui est la plus grande. Les propriétés **que LPropCompareProp** compare n’ont pas besoin d’appartenir au même objet. 
  

