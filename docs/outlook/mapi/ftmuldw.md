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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 861a48464193f357224e33eb0348bc7d5372aa10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783382"
---
# <a name="ftmuldw"></a><span data-ttu-id="6f97f-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="6f97f-103">FtMulDw</span></span>

  
  
<span data-ttu-id="6f97f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6f97f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6f97f-105">Multiplie un nombre entier non signé 64 bits en entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6f97f-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f97f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="6f97f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6f97f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6f97f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6f97f-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="6f97f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6f97f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6f97f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6f97f-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="6f97f-110">Called by:</span></span>  <br/> |<span data-ttu-id="6f97f-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="6f97f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="6f97f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f97f-112">Parameters</span></span>

 <span data-ttu-id="6f97f-113">_Multiplicateur_</span><span class="sxs-lookup"><span data-stu-id="6f97f-113">_Multiplier_</span></span>
  
> <span data-ttu-id="6f97f-114">[in] Un mot double contenant le multiplicateur de nombre entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6f97f-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="6f97f-115">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="6f97f-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="6f97f-116">[in] Une structure [FILETIME](filetime.md) qui contient l’entier non signé de 64 bits à multipliées par la valeur dans le paramètre _Multiplicateur_ .</span><span class="sxs-lookup"><span data-stu-id="6f97f-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6f97f-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6f97f-117">Return value</span></span>

<span data-ttu-id="6f97f-118">La fonction **FtMulDw** renvoie une structure **FILETIME** qui contient le produit de deux entiers.</span><span class="sxs-lookup"><span data-stu-id="6f97f-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="6f97f-119">Les deux paramètres d’entrée restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="6f97f-119">The two input parameters remain unchanged.</span></span> 
  

