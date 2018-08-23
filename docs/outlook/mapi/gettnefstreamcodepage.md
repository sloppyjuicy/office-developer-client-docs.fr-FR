---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d00a2ce3ebec24ca69875bdcb83066d8b891137a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585954"
---
# <a name="gettnefstreamcodepage"></a><span data-ttu-id="361c4-103">GetTnefStreamCodepage</span><span class="sxs-lookup"><span data-stu-id="361c4-103">GetTnefStreamCodepage</span></span>

  
  
<span data-ttu-id="361c4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="361c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="361c4-105">Détermine la page de codes pour un flux de Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="361c4-105">Determines the code page for a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="361c4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="361c4-106">Header file:</span></span>  <br/> |<span data-ttu-id="361c4-107">TNEF.h</span><span class="sxs-lookup"><span data-stu-id="361c4-107">tnef.h</span></span>  <br/> |
|<span data-ttu-id="361c4-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="361c4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="361c4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="361c4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="361c4-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="361c4-110">Called by:</span></span>  <br/> |<span data-ttu-id="361c4-111">Applications clientes et des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="361c4-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a><span data-ttu-id="361c4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="361c4-112">Parameters</span></span>

 <span data-ttu-id="361c4-113">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="361c4-113">_lpStream_</span></span>
  
> <span data-ttu-id="361c4-114">[in] Pointeur vers une flux de données de stockage objet interface OLE **IStream** fournissant une source d’un message de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="361c4-114">[in] Pointer to a storage stream object OLE **IStream** interface providing a source for a TNEF stream message.</span></span> 
    
 <span data-ttu-id="361c4-115">_lpulCodepage_</span><span class="sxs-lookup"><span data-stu-id="361c4-115">_lpulCodepage_</span></span>
  
> <span data-ttu-id="361c4-116">[out] Pointeur vers la page de code de l’objet stream.</span><span class="sxs-lookup"><span data-stu-id="361c4-116">[out] Pointer to the code page of the stream.</span></span>
    
 <span data-ttu-id="361c4-117">_lpulSubCodepage_</span><span class="sxs-lookup"><span data-stu-id="361c4-117">_lpulSubCodepage_</span></span>
  
> <span data-ttu-id="361c4-118">[out] Pointeur vers la page subcode du flux.</span><span class="sxs-lookup"><span data-stu-id="361c4-118">[out] Pointer to the subcode page of the stream.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="361c4-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="361c4-119">Return value</span></span>

 <span data-ttu-id="361c4-120">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="361c4-120">**S_OK**</span></span>
  
> <span data-ttu-id="361c4-121">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="361c4-121">The call succeeded and has returned the expected value or values.</span></span>
    
 <span data-ttu-id="361c4-122">**MAPI_E_NOT_ENOUGH_DISK**</span><span class="sxs-lookup"><span data-stu-id="361c4-122">**MAPI_E_NOT_ENOUGH_DISK**</span></span>
  
> <span data-ttu-id="361c4-123">Une erreur de lecture d’un attribut dans le flux TNEF est survenu.</span><span class="sxs-lookup"><span data-stu-id="361c4-123">There was an error reading an attribute in the TNEF stream.</span></span>
    
 <span data-ttu-id="361c4-124">**MAPI_E_CORRUPT_DATA**</span><span class="sxs-lookup"><span data-stu-id="361c4-124">**MAPI_E_CORRUPT_DATA**</span></span>
  
> <span data-ttu-id="361c4-125">Le flux n’était pas un flux TNEF ou il s’est produit une erreur de lecture de l’attribut attOemCodepage.</span><span class="sxs-lookup"><span data-stu-id="361c4-125">Either the stream was not a TNEF stream or there was an error reading the attOemCodepage attribute.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="361c4-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="361c4-126">Remarks</span></span>

<span data-ttu-id="361c4-127">Utilisez la fonction **GetTnefStreamCodepage** pour lire l’attribut **attOemCodepage** de l’objet stream TNEF pour déterminer la page de code et la page subcode.</span><span class="sxs-lookup"><span data-stu-id="361c4-127">Use the **GetTnefStreamCodepage** function to read the **attOemCodepage** attribute of the TNEF stream to determine the code page and subcode page.</span></span> <span data-ttu-id="361c4-128">Si **attOemCodepage** est introuvable, **GetTnefStreamCodepage** renvoie une page de codes de 437 et une page subcode 0.</span><span class="sxs-lookup"><span data-stu-id="361c4-128">If **attOemCodepage** is not found, **GetTnefStreamCodepage** returns a code page of 437 and a subcode page of 0.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="361c4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="361c4-129">See also</span></span>



[<span data-ttu-id="361c4-130">attOemCodepage</span><span class="sxs-lookup"><span data-stu-id="361c4-130">attOemCodepage</span></span>](http://msdn.microsoft.com/en-us/library/ee158667%28EXCHG.80%29.aspx)

