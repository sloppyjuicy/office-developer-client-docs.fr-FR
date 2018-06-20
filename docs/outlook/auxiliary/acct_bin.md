---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Une variable de ce type de données contient une valeur binaire.
ms.openlocfilehash: 6816fd21a51b86bda97353034e959685f22ff176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782557"
---
# <a name="acctbin"></a><span data-ttu-id="8f81e-103">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="8f81e-103">ACCT_BIN</span></span>

<span data-ttu-id="8f81e-104">Une variable de ce type de données contient une valeur binaire.</span><span class="sxs-lookup"><span data-stu-id="8f81e-104">A variable of this data type holds a binary value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8f81e-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="8f81e-105">Quick info</span></span>

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a><span data-ttu-id="8f81e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8f81e-106">Members</span></span>

<span data-ttu-id="8f81e-107">_cb_</span><span class="sxs-lookup"><span data-stu-id="8f81e-107">_cb_</span></span>
  
> <span data-ttu-id="8f81e-108">Nombre d’octets qui _po_ pointe vers.</span><span class="sxs-lookup"><span data-stu-id="8f81e-108">Number of bytes that  _pb_ points to.</span></span> 
    
<span data-ttu-id="8f81e-109">_pb_</span><span class="sxs-lookup"><span data-stu-id="8f81e-109">_pb_</span></span>
  
> <span data-ttu-id="8f81e-110">Pointeur vers les informations binaires.</span><span class="sxs-lookup"><span data-stu-id="8f81e-110">Pointer to binary information.</span></span>
    

