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
# <a name="ftaddft"></a><span data-ttu-id="5168a-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="5168a-103">FtAddFt</span></span>

  
  
<span data-ttu-id="5168a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5168a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5168a-105">Ajoute un integer 64 bits non signé à un autre.</span><span class="sxs-lookup"><span data-stu-id="5168a-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5168a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5168a-106">Header file:</span></span>  <br/> |<span data-ttu-id="5168a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5168a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5168a-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="5168a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5168a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5168a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5168a-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="5168a-110">Called by:</span></span>  <br/> |<span data-ttu-id="5168a-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="5168a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="5168a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5168a-112">Parameters</span></span>

 <span data-ttu-id="5168a-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="5168a-113">_Addend1_</span></span>
  
> <span data-ttu-id="5168a-114">[in] Structure [FILETIME](filetime.md) qui contient le premier entière 64 bits non signé à ajouter.</span><span class="sxs-lookup"><span data-stu-id="5168a-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="5168a-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="5168a-115">_Addend2_</span></span>
  
> <span data-ttu-id="5168a-116">[in] Structure **FILETIME** qui contient le deuxième integer 64 bits non signé à ajouter.</span><span class="sxs-lookup"><span data-stu-id="5168a-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5168a-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5168a-117">Return value</span></span>

<span data-ttu-id="5168a-118">La **fonction FtAddFt** renvoie une structure **FILETIME** qui contient la somme des deux nombres entières.</span><span class="sxs-lookup"><span data-stu-id="5168a-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="5168a-119">Les deux paramètres d’entrée restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="5168a-119">The two input parameters remain unchanged.</span></span> 
  

