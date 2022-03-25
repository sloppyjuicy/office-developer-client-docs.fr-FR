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
ms.openlocfilehash: 9bc75182658f14aabbcac3d61af5a295481533f3
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782377"
---
# <a name="getinstance"></a>GetInstance

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie une valeur dans une propriété à valeurs multiples dans une propriété à valeur unique du même type. 
  
|Propriété|Valeur|
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
  
> [in] Numéro d’instance, c’est-à-dire, l’élément de tableau, de la valeur copiée à partir de la structure indiquée par le  _paramètre pvalMv_ . 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si la valeur copiée est trop importante pour la mémoire allouée, la fonction **GetInstance** copie uniquement les pointeurs au lieu d’allouer une nouvelle mémoire. 
  

