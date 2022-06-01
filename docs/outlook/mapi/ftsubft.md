---
title: FtSubFt
description: Décrit FtSubFt et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
ms.openlocfilehash: c1acb5289e946b5bdab78d6e5dee3f0d2ae4d805
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816947"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Soustrait un entier 64 bits non signé d’un autre. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Paramètres

 _Minuend_
  
> [in] Structure [FILETIME](filetime.md) qui contient l’entier 64 bits non signé à partir duquel la valeur du paramètre _Subtrahend_ doit être soustraite. 
    
 _Soustrahend_
  
> [in] Structure **FILETIME** qui contient l’entier 64 bits non signé qui est soustrait de la valeur indiquée par le paramètre  _Minuend_ . 
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtSubFt** retourne une structure **FILETIME** qui contient le résultat de la soustraction. Les deux paramètres d’entrée restent inchangés. 
  

