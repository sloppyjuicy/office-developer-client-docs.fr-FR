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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327978"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="fa50e-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="fa50e-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="fa50e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa50e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa50e-105">Multiplie un entier non signé 32 bits par un autre.</span><span class="sxs-lookup"><span data-stu-id="fa50e-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa50e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fa50e-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa50e-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="fa50e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fa50e-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="fa50e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa50e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fa50e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fa50e-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="fa50e-110">Called by:</span></span>  <br/> |<span data-ttu-id="fa50e-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="fa50e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="fa50e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa50e-112">Parameters</span></span>

 <span data-ttu-id="fa50e-113">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="fa50e-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="fa50e-114">dans Mot double qui contient l'entier non signé 32 bits à multiplier par la valeur dans le paramètre _multiplicateur_ .</span><span class="sxs-lookup"><span data-stu-id="fa50e-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="fa50e-115">_Multiplicateur_</span><span class="sxs-lookup"><span data-stu-id="fa50e-115">_Multiplier_</span></span>
  
> <span data-ttu-id="fa50e-116">dans Un double mot qui contient le multiplicateur de nombres entiers non signés 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fa50e-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa50e-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fa50e-117">Return value</span></span>

<span data-ttu-id="fa50e-118">La fonction **FtMulDwDw** renvoie une structure [fileTime](filetime.md) qui contient le produit des deux entiers.</span><span class="sxs-lookup"><span data-stu-id="fa50e-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="fa50e-119">Les deux paramètres d'entrée restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="fa50e-119">The two input parameters remain unchanged.</span></span> 
  

