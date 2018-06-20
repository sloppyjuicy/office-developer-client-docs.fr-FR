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
# <a name="acctvariant"></a><span data-ttu-id="3000f-103">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="3000f-103">ACCT_VARIANT</span></span>

<span data-ttu-id="3000f-104">Une variable de ce type de données contienne la valeur de propriété, qui est un type de données variant.</span><span class="sxs-lookup"><span data-stu-id="3000f-104">A variable of this data type holds the value of a property, which is of a variant data type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3000f-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3000f-105">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="3000f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="3000f-106">Members</span></span>

<span data-ttu-id="3000f-107">_dwType_</span><span class="sxs-lookup"><span data-stu-id="3000f-107">_dwType_</span></span>
  
> <span data-ttu-id="3000f-108">Type de variante :</span><span class="sxs-lookup"><span data-stu-id="3000f-108">Type of variant:</span></span>
    
    - <span data-ttu-id="3000f-109">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3000f-109">PT_LONG</span></span>
    
    - <span data-ttu-id="3000f-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3000f-110">PT_UNICODE</span></span>
    
    - <span data-ttu-id="3000f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3000f-111">PT_BINARY</span></span>
    
<span data-ttu-id="3000f-112">_Data Warehouse_</span><span class="sxs-lookup"><span data-stu-id="3000f-112">_dw_</span></span>
  
> <span data-ttu-id="3000f-113">Valeur DWORD de type variant.</span><span class="sxs-lookup"><span data-stu-id="3000f-113">DWORD value of variant.</span></span>
    
<span data-ttu-id="3000f-114">_pwsz_</span><span class="sxs-lookup"><span data-stu-id="3000f-114">_pwsz_</span></span>
  
> <span data-ttu-id="3000f-115">Valeur de chaîne de type variant.</span><span class="sxs-lookup"><span data-stu-id="3000f-115">String value of variant.</span></span>
    
<span data-ttu-id="3000f-116">_Corbeille_</span><span class="sxs-lookup"><span data-stu-id="3000f-116">_bin_</span></span>
  
> <span data-ttu-id="3000f-117">Valeur binaire de la variante.</span><span class="sxs-lookup"><span data-stu-id="3000f-117">Binary value of the variant.</span></span>
    

