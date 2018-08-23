---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578261"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Soustrait un entier non signé 64 bits d’un autre. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a>Paramètres

 _Minuend_
  
> [in] Une structure [FILETIME](filetime.md) qui contient l’entier non signé de 64 bits à partir de laquelle la valeur dans le paramètre _diminuteur_ est soustraite. 
    
 _Diminuteur_
  
> [in] Une structure **FILETIME** qui contient l’entier non signé de 64 bits qui est soustraite de la valeur indiquée par le paramètre _Minuend_ . 
    
## <a name="return-value"></a>Valeur renvoy�e

La fonction **FtSubFt** renvoie une structure **FILETIME** qui contient le résultat de la soustraction. Les deux paramètres d’entrée restent inchangées. 
  

