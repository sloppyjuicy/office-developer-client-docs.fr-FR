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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300391"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Soustrait un entier non signé 64 bits d'un autre. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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
  
> dans Une structure [fileTime](filetime.md) qui contient l'entier non signé 64 bits à partir duquel la valeur du paramètre _subtrahend_ doit être soustraite. 
    
 _Subtrahend_
  
> dans Une structure **fileTime** qui contient l'entier non signé 64 bits qui est soustrait de la valeur indiquée par le paramètre _minuend_ . 
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtSubFt** renvoie une structure **fileTime** qui contient le résultat de la soustraction. Les deux paramètres d'entrée restent inchangés. 
  

