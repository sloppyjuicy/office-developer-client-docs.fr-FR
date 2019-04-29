---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423383"
---
# <a name="ftnegft"></a><span data-ttu-id="67acd-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="67acd-103">FtNegFt</span></span>

  
  
<span data-ttu-id="67acd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67acd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67acd-105">Calcule le complément à deux d'un entier non signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="67acd-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="67acd-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="67acd-106">Header file:</span></span>  <br/> |<span data-ttu-id="67acd-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="67acd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="67acd-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="67acd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="67acd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="67acd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="67acd-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="67acd-110">Called by:</span></span>  <br/> |<span data-ttu-id="67acd-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="67acd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="67acd-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67acd-112">Parameters</span></span>

 <span data-ttu-id="67acd-113">_pied_</span><span class="sxs-lookup"><span data-stu-id="67acd-113">_ft_</span></span>
  
> <span data-ttu-id="67acd-114">dans Une structure [fileTime](filetime.md) qui contient l'entier non signé 64 bits pour lequel calculer le complément à deux.</span><span class="sxs-lookup"><span data-stu-id="67acd-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="67acd-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="67acd-115">Return value</span></span>

<span data-ttu-id="67acd-116">La fonction **FtNegFt** renvoie une structure **fileTime** qui contient le complément à deux de l'entier.</span><span class="sxs-lookup"><span data-stu-id="67acd-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="67acd-117">Le paramètre d'entrée reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="67acd-117">The input parameter remains unchanged.</span></span> 
  

