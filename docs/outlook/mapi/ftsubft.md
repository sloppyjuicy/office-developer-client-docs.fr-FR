---
title: FtSubFt
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e2ec63b1bd22e22cf3cb6c8e3ef72d1bcfc2c86c
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782873"
---
# <a name="ftsubft"></a>FtSubFt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Soustrait un integer 64 bits non signé d’un autre. 
  
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
    
 _Subtrahend_
  
> [in] Structure **FILETIME** qui contient l’entier 64 bits non signé qui est soustrait de la valeur indiquée par le  _paramètre Minuend_ . 
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction FtSubFt** renvoie une structure **FILETIME** qui contient le résultat de la soustraction. Les deux paramètres d’entrée restent inchangés. 
  

