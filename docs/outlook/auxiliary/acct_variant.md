---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Une variable de ce type de données contient la valeur d’une propriété, qui est d’un type de données variant.
ms.openlocfilehash: 07b6280d7f2dd710375fe59a1811fdd3bb87b695
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621170"
---
# <a name="acct_variant"></a>ACCT_VARIANT

Une variable de ce type de données contient la valeur d’une propriété, qui est d’un type de données variant.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct 
    { 
        DWORD dwType; 
        union  
            { 
            DWORD dw; 
            WCHAR *pwsz; 
            ACCT_BIN bin; 
            } Val; 
    } ACCT_VARIANT; 

```

## <a name="members"></a>Membres

_dwType_
  
> Type de variante :
    
  - PT_LONG
  - PT_UNICODE
  - PT_BINARY
    
_dw_
  
> Valeur DWORD de variante.
    
_pwsz_
  
> Valeur de chaîne de variante.
    
_bin_
  
> Valeur binaire de la variante.
    

