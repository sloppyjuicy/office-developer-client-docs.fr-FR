---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b0260ffe5dc4806cb627fd71c78866bf96796455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434717"
---
# <a name="fbadcolumnset"></a>FBadColumnSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Teste la validité d'un jeu de colonnes de table en vue d'une utilisation par un fournisseur de services lors d'un appel ultérieur à la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a>Paramètres

 _lpptaCols_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété qui définissent les colonnes de tableau à valider. 
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Le jeu de colonnes spécifié n'est pas valide. 
    
FALSE 
  
> Le jeu de colonnes spécifié est valide.
    
## <a name="remarks"></a>Remarques

La fonction **FBadColumnSet** traite les colonnes de type PT_ERROR comme non valides et les colonnes de type PT_NULL comme valides. 
  

