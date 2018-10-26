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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 09c6540f2a224b7dc89a62c34cfb0c867cef4632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570848"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine si les deux MAPI nommée des propriétés sont les mêmes. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] Pointeur vers une structure **MAPINAMEID** décrivant la seconde propriété nommée. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Les noms des deux propriétés sont les mêmes. 
    
FALSE 
  
> Les noms de deux propriété ne correspondent pas.
    
## <a name="remarks"></a>Remarques

La fonction **FEqualNames** est utile car la structure **MAPINAMEID** contient un [GUID](guid.md) et peut représenter le nom de la propriété de plusieurs façons. Cela signifie que les deux structures ne peuvent être ouverts par les méthodes binaires simples. 
  
Le processus de test respecte la casse pour les chaînes de nom de propriété. 
  

