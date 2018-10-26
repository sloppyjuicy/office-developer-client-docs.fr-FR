---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ad561bd3be7fd0c9f25c11875f62667563dfcbe7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578261"
---
# <a name="ftsubft"></a><span data-ttu-id="fc7cf-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="fc7cf-103">FtSubFt</span></span>

  
  
<span data-ttu-id="fc7cf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc7cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc7cf-105">Soustrait un entier non signé 64 bits d’un autre.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fc7cf-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fc7cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc7cf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fc7cf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fc7cf-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="fc7cf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc7cf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fc7cf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fc7cf-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="fc7cf-110">Called by:</span></span>  <br/> |<span data-ttu-id="fc7cf-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="fc7cf-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="fc7cf-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc7cf-112">Parameters</span></span>

 <span data-ttu-id="fc7cf-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="fc7cf-113">_Minuend_</span></span>
  
> <span data-ttu-id="fc7cf-114">[in] Une structure [FILETIME](filetime.md) qui contient l’entier non signé de 64 bits à partir de laquelle la valeur dans le paramètre _diminuteur_ est soustraite.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="fc7cf-115">_Diminuteur_</span><span class="sxs-lookup"><span data-stu-id="fc7cf-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="fc7cf-116">[in] Une structure **FILETIME** qui contient l’entier non signé de 64 bits qui est soustraite de la valeur indiquée par le paramètre _Minuend_ .</span><span class="sxs-lookup"><span data-stu-id="fc7cf-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fc7cf-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fc7cf-117">Return value</span></span>

<span data-ttu-id="fc7cf-118">La fonction **FtSubFt** renvoie une structure **FILETIME** qui contient le résultat de la soustraction.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="fc7cf-119">Les deux paramètres d’entrée restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="fc7cf-119">The two input parameters remain unchanged.</span></span> 
  

