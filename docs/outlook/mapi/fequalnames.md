---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334880"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine si deux propriétés nommées MAPI sont identiques. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Paramètres

 _lpName1_
  
> dans Pointeur vers une structure [MAPINAMEID](mapinameid.md) décrivant la première propriété nommée. 
    
 _lpName2_
  
> dans Pointeur vers une structure **MAPINAMEID** décrivant la deuxième propriété nommée. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Les deux noms de propriété sont égaux. 
    
FALSE 
  
> Les deux noms de propriété ne sont pas égaux.
    
## <a name="remarks"></a>Remarques

La fonction **FEqualNames** est utile, car la structure **MAPINAMEID** contient un [GUID](guid.md) et peut représenter le nom de la propriété lui-même de plusieurs façons. Cela signifie que les deux structures ne peuvent pas être comparées par des méthodes binaires simples. 
  
Le processus de test respecte la casse pour les chaînes de noms de propriétés. 
  

