---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412911"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="fb159-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="fb159-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="fb159-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb159-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb159-105">Multiplie un nombre integer 32 bits non signé par un autre.</span><span class="sxs-lookup"><span data-stu-id="fb159-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb159-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fb159-106">Header file:</span></span>  <br/> |<span data-ttu-id="fb159-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fb159-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fb159-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="fb159-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fb159-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fb159-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fb159-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="fb159-110">Called by:</span></span>  <br/> |<span data-ttu-id="fb159-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="fb159-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="fb159-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="fb159-112">Parameters</span></span>

 <span data-ttu-id="fb159-113">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="fb159-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="fb159-114">[in] Mot double qui contient l’integer 32 bits non signé  à multiplier par la valeur du paramètre Multiplicateur.</span><span class="sxs-lookup"><span data-stu-id="fb159-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="fb159-115">_Multiplicateur_</span><span class="sxs-lookup"><span data-stu-id="fb159-115">_Multiplier_</span></span>
  
> <span data-ttu-id="fb159-116">[in] Mot double qui contient le multiplicateur d’nombres integer 32 bits non signé.</span><span class="sxs-lookup"><span data-stu-id="fb159-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fb159-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fb159-117">Return value</span></span>

<span data-ttu-id="fb159-118">La **fonction FtMulDwDw** renvoie une structure [FILETIME](filetime.md) qui contient le produit des deux nombres entières.</span><span class="sxs-lookup"><span data-stu-id="fb159-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="fb159-119">Les deux paramètres d’entrée restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="fb159-119">The two input parameters remain unchanged.</span></span> 
  

