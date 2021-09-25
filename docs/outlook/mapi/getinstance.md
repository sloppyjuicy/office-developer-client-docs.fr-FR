---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f320ebf3311e2227a2969086606d3b3e592d6e63
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551568"
---
# <a name="getinstance"></a>GetInstance

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie une valeur dans une propriété à valeurs multiples dans une propriété à valeur unique du même type. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIUTIL. H  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Paramètres

 _pvalMv_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définissant une propriété à valeurs multiples. 
    
 _pvalSv_
  
> [in] Pointeur vers une propriété à valeur unique pour recevoir des données. 
    
 _uliInst_
  
> [in] Numéro d’instance, c’est-à-dire, l’élément de tableau, de la valeur copiée à partir de la structure indiquée par le _paramètre pvalMv._ 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si la valeur copiée est trop importante pour la mémoire allouée, la fonction **GetInstance** copie uniquement les pointeurs au lieu d’allouer une nouvelle mémoire. 
  

