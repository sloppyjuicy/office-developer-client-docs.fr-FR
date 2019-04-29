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
# <a name="acctvariant"></a><span data-ttu-id="a8781-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="a8781-103">ACCT_VARIANT</span></span>

<span data-ttu-id="a8781-104">Une variable de ce type de données contient la valeur d'une propriété, qui est de type Variant.</span><span class="sxs-lookup"><span data-stu-id="a8781-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a8781-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a8781-105">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="a8781-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a8781-106">Members</span></span>

<span data-ttu-id="a8781-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="a8781-107">_dwType_</span></span>
  
> <span data-ttu-id="a8781-108">Type de variante:</span><span class="sxs-lookup"><span data-stu-id="a8781-108">Type of variant:</span></span>
    
    - <span data-ttu-id="a8781-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a8781-109">PT_LONG</span></span>
    
    - <span data-ttu-id="a8781-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a8781-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="a8781-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a8781-111">PT_BINARY</span></span>
    
<span data-ttu-id="a8781-112">_warehous_</span><span class="sxs-lookup"><span data-stu-id="a8781-112">_dw_</span></span>
  
> <span data-ttu-id="a8781-113">Valeur DWORD de variant.</span><span class="sxs-lookup"><span data-stu-id="a8781-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="a8781-114">_PWSZ_</span><span class="sxs-lookup"><span data-stu-id="a8781-114">_pwsz_</span></span>
  
> <span data-ttu-id="a8781-115">Valeur de chaîne variant.</span><span class="sxs-lookup"><span data-stu-id="a8781-115">String value of variant.</span></span>
    
<span data-ttu-id="a8781-116">_plateau_</span><span class="sxs-lookup"><span data-stu-id="a8781-116">_bin_</span></span>
  
> <span data-ttu-id="a8781-117">Valeur binaire de la variante.</span><span class="sxs-lookup"><span data-stu-id="a8781-117">Binary value of the variant.</span></span>
    

