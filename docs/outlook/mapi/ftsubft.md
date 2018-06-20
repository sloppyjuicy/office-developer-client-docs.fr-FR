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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 954630b0b92772d961dc61084c28a9ab419e4c2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783392"
---
# <a name="ftsubft"></a><span data-ttu-id="b7943-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="b7943-103">FtSubFt</span></span>

  
  
<span data-ttu-id="b7943-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7943-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7943-105">Soustrait un entier non signé 64 bits d’un autre.</span><span class="sxs-lookup"><span data-stu-id="b7943-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7943-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b7943-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7943-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b7943-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b7943-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="b7943-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b7943-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b7943-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b7943-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="b7943-110">Called by:</span></span>  <br/> |<span data-ttu-id="b7943-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b7943-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="b7943-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7943-112">Parameters</span></span>

 <span data-ttu-id="b7943-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="b7943-113">_Minuend_</span></span>
  
> <span data-ttu-id="b7943-114">[in] Une structure [FILETIME](filetime.md) qui contient l’entier non signé de 64 bits à partir de laquelle la valeur dans le paramètre _diminuteur_ est soustraite.</span><span class="sxs-lookup"><span data-stu-id="b7943-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="b7943-115">_Diminuteur_</span><span class="sxs-lookup"><span data-stu-id="b7943-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="b7943-116">[in] Une structure **FILETIME** qui contient l’entier non signé de 64 bits qui est soustraite de la valeur indiquée par le paramètre _Minuend_ .</span><span class="sxs-lookup"><span data-stu-id="b7943-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b7943-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b7943-117">Return value</span></span>

<span data-ttu-id="b7943-118">La fonction **FtSubFt** renvoie une structure **FILETIME** qui contient le résultat de la soustraction.</span><span class="sxs-lookup"><span data-stu-id="b7943-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="b7943-119">Les deux paramètres d’entrée restent inchangées.</span><span class="sxs-lookup"><span data-stu-id="b7943-119">The two input parameters remain unchanged.</span></span> 
  

