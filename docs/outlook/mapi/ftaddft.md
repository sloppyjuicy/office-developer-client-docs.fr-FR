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
ms.openlocfilehash: e0e1535a770d4f1b437faf6a90c5f6415f6000ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783389"
---
# <a name="ftaddft"></a><span data-ttu-id="5e56f-103">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="5e56f-103">FtAddFt</span></span>

  
  
<span data-ttu-id="5e56f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e56f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e56f-105">Ajoute un entier non signé de 64 bits à un autre.</span><span class="sxs-lookup"><span data-stu-id="5e56f-105">Adds one unsigned 64-bit integer to another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e56f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5e56f-106">Header file:</span></span>  <br/> |<span data-ttu-id="5e56f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5e56f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5e56f-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="5e56f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5e56f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5e56f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5e56f-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="5e56f-110">Called by:</span></span>  <br/> |<span data-ttu-id="5e56f-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="5e56f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAddFt(
  FILETIME Addend1,
  FILETIME Addend2
);
```

## <a name="parameters"></a><span data-ttu-id="5e56f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e56f-112">Parameters</span></span>

 <span data-ttu-id="5e56f-113">_Addend1_</span><span class="sxs-lookup"><span data-stu-id="5e56f-113">_Addend1_</span></span>
  
> <span data-ttu-id="5e56f-114">[in] Une structure [FILETIME](filetime.md) qui contient le premier entier non signé 64 bits à ajouter.</span><span class="sxs-lookup"><span data-stu-id="5e56f-114">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="5e56f-115">_Addend2_</span><span class="sxs-lookup"><span data-stu-id="5e56f-115">_Addend2_</span></span>
  
> <span data-ttu-id="5e56f-116">[in] Une structure **FILETIME** qui contient le deuxième entier 64 bits non signé à ajouter.</span><span class="sxs-lookup"><span data-stu-id="5e56f-116">[in] A **FILETIME** structure that contains the second unsigned 64-bit integer to be added.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5e56f-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="5e56f-117">Return value</span></span>

<span data-ttu-id="5e56f-118">La fonction **FtAddFt** renvoie une structure **FILETIME** qui contient la somme de deux entiers.</span><span class="sxs-lookup"><span data-stu-id="5e56f-118">The **FtAddFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="5e56f-119">Les deux paramètres d’entrée restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="5e56f-119">The two input parameters remain unchanged.</span></span> 
  

