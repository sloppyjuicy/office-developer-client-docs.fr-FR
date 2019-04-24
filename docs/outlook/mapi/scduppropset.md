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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351267"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Duplique un tableau de valeurs de propriété dans un bloc unique de mémoire MAPI qui combine les opérations des fonctions [ScCopyProps](sccopyprops.md) et [ScCountProps](sccountprops.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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

## <a name="parameters"></a>Paramètres

 _cprop_
  
> dans Nombre de valeurs de propriété dans le tableau indiqué par le paramètre _rgprop_ . 
    
 _rgprop_
  
> dans Pointeur vers un tableau de structures [SPropValue](spropvalue.md) définissant les valeurs de propriété à dupliquer. 
    
 _lpAllocateBuffer_
  
> dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire pour le tableau dupliqué. 
    
 _prgprop_
  
> remarquer Pointeur vers la position initiale dans la mémoire où le tableau de structures **SPropValue** en double renvoyé est stocké. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    

