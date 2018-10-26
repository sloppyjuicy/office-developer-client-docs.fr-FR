---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c823a4e3d08d9082a3b5ac5c4bd8169612caa16e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583994"
---
# <a name="ftmuldw"></a><span data-ttu-id="f5cab-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="f5cab-103">FtMulDw</span></span>

  
  
<span data-ttu-id="f5cab-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5cab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5cab-105">Multiplie un nombre entier non signé 64 bits en entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f5cab-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5cab-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f5cab-106">Header file:</span></span>  <br/> |<span data-ttu-id="f5cab-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f5cab-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f5cab-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f5cab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f5cab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f5cab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f5cab-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f5cab-110">Called by:</span></span>  <br/> |<span data-ttu-id="f5cab-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f5cab-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="f5cab-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5cab-112">Parameters</span></span>

 <span data-ttu-id="f5cab-113">_Multiplicateur_</span><span class="sxs-lookup"><span data-stu-id="f5cab-113">_Multiplier_</span></span>
  
> <span data-ttu-id="f5cab-114">[in] Un mot double contenant le multiplicateur de nombre entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f5cab-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="f5cab-115">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="f5cab-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="f5cab-116">[in] Une structure [FILETIME](filetime.md) qui contient l’entier non signé de 64 bits à multipliées par la valeur dans le paramètre _Multiplicateur_ .</span><span class="sxs-lookup"><span data-stu-id="f5cab-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f5cab-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f5cab-117">Return value</span></span>

<span data-ttu-id="f5cab-118">La fonction **FtMulDw** renvoie une structure **FILETIME** qui contient le produit de deux entiers.</span><span class="sxs-lookup"><span data-stu-id="f5cab-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="f5cab-119">Les deux paramètres d’entrée restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="f5cab-119">The two input parameters remain unchanged.</span></span> 
  

