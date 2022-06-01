---
title: GetInstance
description: Décrit GetInstance et fournit la syntaxe, les paramètres et la valeur de retour.
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
ms.openlocfilehash: 4fcdf88518f4a0e3301a5970852573cf80928208
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817080"
---
# <a name="getinstance"></a>GetInstance

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie une valeur dans une propriété à valeurs multiples vers une propriété à valeur unique du même type. 
  
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
  
> [in] Numéro d’instance, c’est-à-dire l’élément de tableau, de la valeur copiée à partir de la structure indiquée par le paramètre  _pvalMv_ . 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Si la valeur copiée est trop grande pour la mémoire allouée, la fonction **GetInstance** copie uniquement les pointeurs au lieu d’allouer de la nouvelle mémoire. 
  

