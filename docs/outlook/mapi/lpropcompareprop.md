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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357434"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux valeurs de propriété pour déterminer si elles sont égales. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Paramètres

 _lpSPropValueA_
  
> dans Pointeur vers une structure [SPropValue](spropvalue.md) définissant la valeur de la première propriété à comparer. 
    
 _lpSPropValueB_
  
> dans Pointeur vers une structure **SPropValue** définissant la deuxième valeur de propriété à comparer. 
    
## <a name="return-value"></a>Valeur renvoyée

 **LPropCompareProp** renvoie l'une des valeurs suivantes pour la plupart des types de propriétés: 
  
- Inférieur à zéro si la valeur indiquée par le paramètre _lpSPropValueA_ est inférieure à celle indiquée par le paramètre _lpSPropValueB_ . 
    
- Supérieur à zéro si la valeur indiquée par _lpSPropValueA_ est supérieure à celle indiquée par _lpSPropValueB_.
    
- Zéro si la valeur indiquée par _lpSPropValueA_ est égale à la valeur indiquée par _lpSPropValueB_. 
    
Pour les types de propriétés qui n'ont pas d'ordre intrinsèque, tels que les types Boolean ou Error, la fonction **LPropCompareProp** renvoie une valeur non définie si les deux valeurs de propriété ne sont pas égales. Cette valeur non définie est différente de zéro et est cohérente entre les appels. 
  
## <a name="remarks"></a>Remarques

Utilisez la fonction **LPropCompareProp** uniquement si les types des deux propriétés à comparer sont les mêmes. 
  
Avant d'appeler **LPropCompareProp**, une application cliente ou un fournisseur de services doit d'abord récupérer les propriétés pour les comparer à l'aide d'un appel à la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) . Lorsqu'un client ou un fournisseur appelle **LPropCompareProp**, la fonction examine d'abord les balises de propriété pour s'assurer que la comparaison des valeurs de propriété est valide. La fonction compare ensuite les valeurs de propriété, en renvoyant une valeur appropriée. 
  
Si les valeurs de propriété ne sont pas égales, **LPropCompareProp** détermine la valeur la plus élevée. Les propriétés qu' **LPropCompareProp** compare n'ont pas besoin d'appartenir au même objet. 
  

