---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299432"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="d2fdf-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="d2fdf-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="d2fdf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2fdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2fdf-105">Détermine la page de code d'Transport-Neutral flux TNEF (Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="d2fdf-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2fdf-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d2fdf-106">Header file:</span></span>  <br/> |<span data-ttu-id="d2fdf-107">tnef.h</span><span class="sxs-lookup"><span data-stu-id="d2fdf-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="d2fdf-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d2fdf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d2fdf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d2fdf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d2fdf-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d2fdf-110">Called by:</span></span>  <br/> |<span data-ttu-id="d2fdf-111">Applications clientes et fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="d2fdf-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d2fdf-112">Parameters</span></span>

 <span data-ttu-id="d2fdf-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="d2fdf-113">_lpStream_</span></span>
  
> <span data-ttu-id="d2fdf-114">[in] Pointeur vers une interface OLE **IStream** d’objet de flux de stockage fournissant une source pour un message de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="d2fdf-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="d2fdf-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="d2fdf-116">[out] Pointeur vers la page de code du flux.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="d2fdf-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="d2fdf-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="d2fdf-118">[out] Pointeur vers la page de sous-code du flux.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d2fdf-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d2fdf-119">Return value</span></span>

 <span data-ttu-id="d2fdf-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="d2fdf-120">**S_OK**</span></span>
  
> <span data-ttu-id="d2fdf-121">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="d2fdf-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="d2fdf-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="d2fdf-123">Une erreur s’est produite lors de la lecture d’un attribut dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="d2fdf-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="d2fdf-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="d2fdf-125">Le flux n’était pas un flux TNEF ou une erreur s’est produite lors de la lecture de l’attribut attOemCodepage.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2fdf-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2fdf-126">Remarks</span></span>

<span data-ttu-id="d2fdf-127">Utilisez la **fonction GetTnefStreamCodepage** pour lire l’attribut **attOemCodepage** du flux TNEF afin de déterminer la page de code et la page de sous-code.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="d2fdf-128">Si **attOemCodepage** est in found, **GetTnefStreamCodepage** renvoie une page de code 437 et une page de sous-code de 0.</span><span class="sxs-lookup"><span data-stu-id="d2fdf-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2fdf-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2fdf-129">See also</span></span>



[<span data-ttu-id="d2fdf-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="d2fdf-130">attOemCodepage</span></span>](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

