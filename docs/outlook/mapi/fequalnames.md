---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4bb6295ce75c0036aaa8d13cdd8c66acf8cd4c35
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63629516"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine si deux propriétés nommées MAPI sont identiques. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Pointeur vers une structure [MAPINAMEID](mapinameid.md) décrivant la première propriété nommée. 
    
 _lpName2_
  
> [in] Pointeur vers une structure **MAPINAMEID** décrivant la deuxième propriété nommée. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Les deux noms de propriété sont égaux. 
    
FALSE 
  
> Les deux noms de propriété ne sont pas égaux.
    
## <a name="remarks"></a>Remarques

La **fonction FEqualNames est** utile, car la structure **MAPINAMEID** contient un [GUID](guid.md) et peut représenter le nom de la propriété elle-même de plusieurs manières. Cela signifie que les deux structures ne peuvent pas être comparées par des méthodes binaires simples. 
  
Le processus de test est sensible à la cas pour les chaînes de nom de propriété. 
  

