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
ms.openlocfilehash: 37e6560d859ce4731b7a06e571eb38eb160c3686
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417657"
---
# <a name="hrsetoneprop"></a>HrSetOneProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit ou modifie la valeur d'une propriété unique sur une interface de propriété, c'est-à-dire une interface dérivée de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HrSetOneProp(
  LPMAPIPROP pmp,
  LPSPropValue pprop
);
```

## <a name="parameters"></a>Paramètres

 _PMP_
  
> dans Pointeur vers une interface [IMAPIProp](imapipropiunknown.md) sur laquelle la valeur de propriété doit être définie ou modifiée. 
    
 _pprop_
  
> dans Pointeur vers la structure [SPropValue](spropvalue.md) définissant la valeur à définir sur la propriété _PMP_ . 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Contrairement à la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) , la fonction **HrSetOneProp** ne renvoie jamais aucun avertissement. Étant donné qu'elle définit une seule propriété, elle réussit ou échoue. Pour définir ou modifier plusieurs propriétés, **SetProps** est plus rapide. 
  
Vous pouvez récupérer une seule propriété à l'aide de la fonction [HrGetOneProp](hrgetoneprop.md) . 
  

