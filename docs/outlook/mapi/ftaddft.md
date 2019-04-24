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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cb20469adec938817fedf1b00789304625b388c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328006"
---
# <a name="ftaddft"></a><span data-ttu-id="e2a69-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="e2a69-103">FtAddFt</span></span>

  
  
<span data-ttu-id="e2a69-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2a69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2a69-105">Ajoute un entier non signé 64 bits à un autre.</span><span class="sxs-lookup"><span data-stu-id="e2a69-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2a69-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e2a69-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2a69-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e2a69-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e2a69-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e2a69-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e2a69-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e2a69-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e2a69-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e2a69-110">Called by:</span></span>  <br/> |<span data-ttu-id="e2a69-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e2a69-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="e2a69-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2a69-112">Parameters</span></span>

 <span data-ttu-id="e2a69-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="e2a69-113">_Addend1_</span></span>
  
> <span data-ttu-id="e2a69-114">dans Une structure [fileTime](filetime.md) qui contient le premier entier non signé 64 bits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="e2a69-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="e2a69-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="e2a69-115">_Addend2_</span></span>
  
> <span data-ttu-id="e2a69-116">dans Une structure **fileTime** qui contient le deuxième entier non signé 64 bits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="e2a69-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e2a69-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e2a69-117">Return value</span></span>

<span data-ttu-id="e2a69-118">La fonction **FtAddFt** renvoie une structure **fileTime** qui contient la somme des deux entiers.</span><span class="sxs-lookup"><span data-stu-id="e2a69-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="e2a69-119">Les deux paramètres d'entrée restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="e2a69-119">The two input parameters remain unchanged.</span></span> 
  

