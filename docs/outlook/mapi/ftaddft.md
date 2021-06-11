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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404763"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un integer 64 bits non signé à un autre.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a>Parameters

 _Addend1_
  
> [in] Structure [FILETIME](filetime.md) qui contient le premier entière 64 bits non signé à ajouter. 
    
 _Addend2_
  
> [in] Structure **FILETIME** qui contient le deuxième integer 64 bits non signé à ajouter. 
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction FtAddFt** renvoie une structure **FILETIME** qui contient la somme des deux nombres entières. Les deux paramètres d’entrée restent inchangés. 
  

