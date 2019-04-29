---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Une variable de ce type de données contient une valeur binaire.
ms.openlocfilehash: 3dcaaf73a04ddc608e68ca7bd1f801d0a5d99bb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408123"
---
# <a name="acctbin"></a>ACCT_BIN

Une variable de ce type de données contient une valeur binaire.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a>Membres

_cb_
  
> Nombre d'octets vers lesquels pointe _PB_ . 
    
_pb_
  
> Pointeur vers des informations binaires.
    

