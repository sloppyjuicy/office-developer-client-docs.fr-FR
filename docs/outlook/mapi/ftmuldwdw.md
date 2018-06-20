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
ms.openlocfilehash: 16dca82b94225afc88bcb6c4e698a50565d6b088
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783386"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="a02b0-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="a02b0-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="a02b0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a02b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a02b0-105">Multiplie un entier non signé de 32 bits par une autre.</span><span class="sxs-lookup"><span data-stu-id="a02b0-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a02b0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a02b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="a02b0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a02b0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a02b0-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="a02b0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a02b0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a02b0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a02b0-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="a02b0-110">Called by:</span></span>  <br/> |<span data-ttu-id="a02b0-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="a02b0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="a02b0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a02b0-112">Parameters</span></span>

 <span data-ttu-id="a02b0-113">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="a02b0-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="a02b0-114">[in] Un mot double contenant le nombre entier non signé 32 bits à multipliées par la valeur dans le paramètre _Multiplicateur_ .</span><span class="sxs-lookup"><span data-stu-id="a02b0-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="a02b0-115">_Multiplicateur_</span><span class="sxs-lookup"><span data-stu-id="a02b0-115">_Multiplier_</span></span>
  
> <span data-ttu-id="a02b0-116">[in] Un mot double contenant le multiplicateur de nombre entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a02b0-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a02b0-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a02b0-117">Return value</span></span>

<span data-ttu-id="a02b0-118">La fonction **FtMulDwDw** renvoie une structure [FILETIME](filetime.md) qui contient le produit de deux entiers.</span><span class="sxs-lookup"><span data-stu-id="a02b0-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="a02b0-119">Les deux paramètres d’entrée restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="a02b0-119">The two input parameters remain unchanged.</span></span> 
  

