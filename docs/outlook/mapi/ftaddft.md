---
title: FtAddFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtAddFt
api_type:
- COM
ms.assetid: 341ad06b-1caa-49bb-b859-cb512f6fb55d
description: Ajoute un integer 64 bits non signé à un autre pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: b7223d8536237e82b7041dcb8536648e63044c4c
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764047"
---
# <a name="ftaddft"></a>FtAddFt

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute un integer 64 bits non signé à un autre.
  
|Propriété |Valeur |
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

## <a name="parameters"></a>Paramètres

 _Addend1_
  
> [in] Structure [FILETIME](filetime.md) qui contient le premier entière 64 bits non signé à ajouter. 
    
 _Addend2_
  
> [in] Structure **FILETIME** qui contient le deuxième integer 64 bits non signé à ajouter. 
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction FtAddFt** renvoie une structure **FILETIME** qui contient la somme des deux nombres entières. Les deux paramètres d’entrée restent inchangés. 
  

