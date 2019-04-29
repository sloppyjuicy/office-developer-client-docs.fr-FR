---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Une variable de ce type de données contient la valeur d'une propriété, qui est de type Variant.
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424398"
---
# <a name="acctvariant"></a>ACCT_VARIANT

Une variable de ce type de données contient la valeur d'une propriété, qui est de type Variant.
  
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
  
> Type de variante:
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_warehous_
  
> Valeur DWORD de variant.
    
_PWSZ_
  
> Valeur de chaîne variant.
    
_plateau_
  
> Valeur binaire de la variante.
    

