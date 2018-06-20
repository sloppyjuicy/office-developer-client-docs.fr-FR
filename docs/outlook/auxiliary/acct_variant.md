---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Une variable de ce type de données contienne la valeur de propriété, qui est un type de données variant.
ms.openlocfilehash: c85af4bd4fefffb4fadf671bb7cf5b7f072d5e95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782549"
---
# <a name="acctvariant"></a>ACCT_VARIANT

Une variable de ce type de données contienne la valeur de propriété, qui est un type de données variant.
  
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
  
> Type de variante :
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_Data Warehouse_
  
> Valeur DWORD de type variant.
    
_pwsz_
  
> Valeur de chaîne de type variant.
    
_Corbeille_
  
> Valeur binaire de la variante.
    

