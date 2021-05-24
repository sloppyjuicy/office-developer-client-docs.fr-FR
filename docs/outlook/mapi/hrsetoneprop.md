---
title: HrSetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSetOneProp
api_type:
- COM
ms.assetid: 14ae3242-fddf-4199-a9a7-4ab153b31064
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9fae06b9e9d5ef4885d798825659fa3486ec9e72
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589179"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit ou modifie la valeur d’une propriété unique sur une interface de propriétés, c’est-à-dire une interface dérivée [d’IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HRESULT HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Parameters

 _pmp_
  
> [in] Pointeur vers une interface [IMAPIProp](imapipropiunknown.md) sur laquelle la valeur de la propriété doit être définie ou modifiée. 
    
 _pprop_
  
> [in] Pointeur vers la structure [SPropValue](spropvalue.md) définissant la valeur à définir sur la _propriété pmp._ 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Contrairement à [la méthode IMAPIProp::SetProps,](imapiprop-setprops.md) la fonction **HrSetOneProp** ne renvoie jamais d’avertissement. Comme elle ne définit qu’une seule propriété, elle réussit ou échoue simplement. Pour définir ou modifier plusieurs propriétés, **SetProps** est plus rapide. 
  
Vous pouvez récupérer une propriété unique avec [la fonction HrGetOneProp.](hrgetoneprop.md) 
  

