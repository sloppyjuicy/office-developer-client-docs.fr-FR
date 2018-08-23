---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c4e5d2847b53988fb75e23fc6c4dfc386ea678f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579262"
---
# <a name="getinstance"></a>GetInstance

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Copie une valeur dans une propriété à valeurs multiples sur une propriété à valeur unique du même type. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIUTIL. H  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Paramètres

 _pvalMv_
  
> [in] Pointeur vers une structure [SPropValue](spropvalue.md) définition d’une propriété à valeurs multiples. 
    
 _pvalSv_
  
> [in] Pointeur vers une propriété à valeur unique de recevoir des données. 
    
 _uliInst_
  
> [in] Le numéro d’instance, c'est-à-dire, l’élément de tableau, de la valeur en cours de copie de la structure indiquée par le paramètre _pvalMv_ . 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si la valeur copiée est trop volumineux pour la mémoire allouée, la fonction **GetInstance** copie uniquement des pointeurs au lieu d’allouer davantage de mémoire. 
  

