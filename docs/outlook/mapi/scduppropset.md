---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406016"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Duplique un tableau de valeurs de propriétés dans un seul bloc de mémoire MAPI combinant les opérations des fonctions [ScCopyProps](sccopyprops.md) et [ScCountProps.](sccountprops.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a>Parameters

 _cprop_
  
> [in] Nombre de valeurs de propriété dans le tableau indiqué par le _paramètre rgprop._ 
    
 _rgprop_
  
> [in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) définissant les valeurs de propriété à dupliquer. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire pour le tableau dupliqué. 
    
 _prgprop_
  
> [out] Pointeur vers la position initiale dans la mémoire où le tableau dupliqué renvoyé des structures **SPropValue** est stocké. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    

