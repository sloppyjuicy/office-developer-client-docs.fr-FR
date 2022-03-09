---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Une variable de ce type de données contient une valeur binaire.
ms.openlocfilehash: dfb25a65fb3cbfab21134f1df33964c11bc0e17d
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370126"
---
# <a name="acct_bin"></a>ACCT_BIN

Une variable de ce type de données contient une valeur binaire.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    DWORD cb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a>Membres

_cb_
  
> Nombre d’octets vers _qui pointe le pb_ .

_pb_
  
> Pointeur vers les informations binaires.
