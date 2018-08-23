---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4b02fc316001ae11d64988cc29d0e62e9adde55e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585583"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ajoute un entier non signé de 64 bits à un autre.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Paramètres

 _Addend1_
  
> [in] Une structure [FILETIME](filetime.md) qui contient le premier entier non signé 64 bits à ajouter. 
    
 _Addend2_
  
> [in] Une structure **FILETIME** qui contient le deuxième entier 64 bits non signé à ajouter. 
    
## <a name="return-value"></a>Valeur renvoy�e

La fonction **FtAddFt** renvoie une structure **FILETIME** qui contient la somme de deux entiers. Les deux paramètres d’entrée restent inchangées. 
  

