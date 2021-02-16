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
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408417"
---
# <a name="ftsubft"></a><span data-ttu-id="f72b1-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="f72b1-103">FtSubFt</span></span>

  
  
<span data-ttu-id="f72b1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f72b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f72b1-105">Soustrait un integer 64 bits non signé d’un autre.</span><span class="sxs-lookup"><span data-stu-id="f72b1-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f72b1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f72b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="f72b1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f72b1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f72b1-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f72b1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f72b1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f72b1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f72b1-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f72b1-110">Called by:</span></span>  <br/> |<span data-ttu-id="f72b1-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f72b1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="f72b1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f72b1-112">Parameters</span></span>

 <span data-ttu-id="f72b1-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="f72b1-113">_Minuend_</span></span>
  
> <span data-ttu-id="f72b1-114">[in] Structure [FILETIME](filetime.md) qui contient l’entier 64 bits non signé à partir duquel la valeur du paramètre  _Subtrahend_ doit être soustraite.</span><span class="sxs-lookup"><span data-stu-id="f72b1-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="f72b1-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="f72b1-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="f72b1-116">[in] Structure **FILETIME** qui contient l’entier 64 bits non signé qui est soustrait de la valeur indiquée par le _paramètre Minuend._</span><span class="sxs-lookup"><span data-stu-id="f72b1-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f72b1-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f72b1-117">Return value</span></span>

<span data-ttu-id="f72b1-118">La **fonction FtSubFt** renvoie une structure **FILETIME** qui contient le résultat de la soustraction.</span><span class="sxs-lookup"><span data-stu-id="f72b1-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="f72b1-119">Les deux paramètres d’entrée restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="f72b1-119">The two input parameters remain unchanged.</span></span> 
  

