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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8af0d5c6eaff0c1e01e01c24c46f299e0c637f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783566"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**S’applique à**: Outlook 
  
Définit ou modifie la valeur d’une seule propriété sur une interface de propriété, autrement dit, une interface dérivée de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Paramètres

 _nous procure_
  
> [in] Pointeur vers une interface [IMAPIProp](imapipropiunknown.md) sur lequel la valeur de la propriété doit être défini ou modifié. 
    
 _pprop_
  
> [in] Pointeur vers la structure [SPropValue](spropvalue.md) définissant la valeur à définir la propriété _nous procure_ . 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Contrairement à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) , la fonction **HrSetOneProp** ne retourne jamais les éventuels avertissements. Parce qu’elle ne définit qu’une seule propriété, il suffit réussit ou échoue. Pour définir ou modifier plusieurs propriétés, **SetProps** est plus rapide. 
  
Vous pouvez récupérer une seule propriété avec la fonction [HrGetOneProp](hrgetoneprop.md) . 
  

