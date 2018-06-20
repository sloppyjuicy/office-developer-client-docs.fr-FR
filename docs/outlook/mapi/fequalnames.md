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
ms.openlocfilehash: 0d8d1b8509f699b20f6e436d8af2c1d0d97cf4ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783294"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**S’applique à**: Outlook 
  
Détermine si les deux MAPI nommée des propriétés sont les mêmes. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> Les noms des deux propriétés sont les mêmes. 
    
FALSE 
  
> Les noms de deux propriété ne correspondent pas.
    
## <a name="remarks"></a>Remarques

La fonction **FEqualNames** est utile car la structure **MAPINAMEID** contient un [GUID](guid.md) et peut représenter le nom de la propriété de plusieurs façons. Cela signifie que les deux structures ne peuvent être ouverts par les méthodes binaires simples. 
  
Le processus de test respecte la casse pour les chaînes de nom de propriété. 
  

