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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581978"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un tableau de valeurs de propriété dans un bloc de mémoire MAPI combinant les opérations des fonctions [ScCopyProps](sccopyprops.md) et [ScCountProps](sccountprops.md) les doublons. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] Nombre de valeurs de propriété dans le tableau indiqué par le paramètre _rgprop_ . 
    
 _rgprop_
  
> [in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) définissant les valeurs de propriété à dupliquer. 
    
 _lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire pour le tableau dupliqué. 
    
 _prgprop_
  
> [out] Pointeur vers la position initiale dans la mémoire où est stockée la matrice renvoyée dupliquée des structures **SPropValue** . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    

