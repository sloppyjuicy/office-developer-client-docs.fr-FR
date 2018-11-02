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
ms.openlocfilehash: 0985ed0c5d4482bb22f46bdc9198afc343c61e5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565535"
---
# <a name="lpropcompareprop"></a>LPropCompareProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux valeurs de propriété pour déterminer si elles sont égales. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a>Paramètres

 _lpSPropValueA_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définition de la première valeur de propriété à comparer. 
    
 _lpSPropValueB_
  
> [in] Pointeur vers une structure **SPropValue** définissant la valeur de la propriété deuxième à comparer. 
    
## <a name="return-value"></a>Valeur renvoyée

 **LPropCompareProp** renvoie une des valeurs suivantes pour la plupart des types de propriété : 
  
- Inférieur à zéro si la valeur indiquée par le paramètre _lpSPropValueA_ est inférieur à celui indiqué par le paramètre _lpSPropValueB_ . 
    
- Supérieure à zéro si la valeur indiquée par _lpSPropValueA_ est supérieure à celle indiquée par _lpSPropValueB_.
    
- Zéro si la valeur indiquée par _lpSPropValueA_ est égale à la valeur indiquée par _lpSPropValueB_. 
    
Pour les types de propriété dont aucun classement intrinsèques, telles que booléen ou erreur, la fonction **LPropCompareProp** renvoie une valeur non définie si les deux valeurs de propriété ne sont pas égales. Cette valeur non définie est différente de zéro et cohérente entre les appels. 
  
## <a name="remarks"></a>Remarques

Utilisez la fonction **LPropCompareProp** uniquement si les types d’à comparer les deux propriétés sont les mêmes. 
  
Avant d’appeler **LPropCompareProp**, une application cliente ou un fournisseur de services doit récupérons d’abord les propriétés pour la comparaison avec un appel à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . Lorsqu’un client ou fournisseur appels **LPropCompareProp**, la fonction examine en premier lieu les balises de propriété pour vous assurer que la comparaison de valeurs de propriété est valide. La fonction compare ensuite les valeurs de propriété, renvoyer une valeur appropriée. 
  
Si les valeurs de propriété ne sont pas égales, **LPropCompareProp** détermine quel est le meilleur. Les propriétés **LPropCompareProp** compare n’ont pas appartenir au même objet. 
  

