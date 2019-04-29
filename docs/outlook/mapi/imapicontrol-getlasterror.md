---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421150"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="46f9a-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="46f9a-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="46f9a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46f9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46f9a-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur de contrôle de bouton précédente.</span><span class="sxs-lookup"><span data-stu-id="46f9a-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="46f9a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46f9a-106">Parameters</span></span>

 <span data-ttu-id="46f9a-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="46f9a-107">_hResult_</span></span>
  
> <span data-ttu-id="46f9a-108">dans Handle de la valeur d'erreur générée lors de l'appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="46f9a-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="46f9a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="46f9a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="46f9a-110">dans Masque de des indicateurs qui contrôle le type des chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="46f9a-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="46f9a-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="46f9a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="46f9a-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="46f9a-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="46f9a-113">Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="46f9a-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="46f9a-114">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="46f9a-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="46f9a-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="46f9a-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="46f9a-116">remarquer Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, de composant et de contexte pour l'erreur.</span><span class="sxs-lookup"><span data-stu-id="46f9a-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="46f9a-117">Le paramètre _lppMAPIError_ peut être défini sur null si le fournisseur ne peut pas fournir une structure **MAPIERROR** avec les informations appropriées.</span><span class="sxs-lookup"><span data-stu-id="46f9a-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="46f9a-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="46f9a-118">Return value</span></span>

<span data-ttu-id="46f9a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="46f9a-119">S_OK</span></span> 
  
> <span data-ttu-id="46f9a-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="46f9a-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="46f9a-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="46f9a-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="46f9a-122">L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="46f9a-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46f9a-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="46f9a-123">Remarks</span></span>

<span data-ttu-id="46f9a-124">Les fournisseurs de services implémentent la méthode **IMAPIControl:: GetLastError** pour fournir des informations sur un appel de la méthode précédent qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="46f9a-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="46f9a-125">MAPI peut donner aux utilisateurs des informations détaillées sur l'erreur en affichant les données de la structure **MAPIERROR** dans un message ou une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="46f9a-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="46f9a-126">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="46f9a-126">Notes to implementers</span></span>

<span data-ttu-id="46f9a-127">Vous n'avez pas besoin d'informations à inclure dans la structure **MAPIERROR** pour chaque erreur.</span><span class="sxs-lookup"><span data-stu-id="46f9a-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="46f9a-128">Il se peut que vous ne soyez pas en mesure de déterminer l'erreur précédente.</span><span class="sxs-lookup"><span data-stu-id="46f9a-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="46f9a-129">Si vous disposez d'informations, retournez S_OK et les données appropriées dans la structure **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="46f9a-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="46f9a-130">Si aucune information n'est disponible, renvoyer S_OK et un pointeur vers NULL pour le paramètre _lppMAPIError_ .</span><span class="sxs-lookup"><span data-stu-id="46f9a-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="46f9a-131">Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [erreurs étendues MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="46f9a-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="46f9a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46f9a-132">See also</span></span>



[<span data-ttu-id="46f9a-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="46f9a-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="46f9a-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="46f9a-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="46f9a-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46f9a-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

