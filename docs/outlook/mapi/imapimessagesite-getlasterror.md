---
title: IMAPIMessageSiteGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetLastError
api_type:
- COM
ms.assetid: 7ea282d7-388a-4f05-9780-f8dbc5c5d395
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3426fd29090a6ab1bb0e66f9bb746e84abe3a25e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589447"
---
# <a name="imapimessagesitegetlasterror"></a><span data-ttu-id="ae3bf-103">IMAPIMessageSite::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ae3bf-103">IMAPIMessageSite::GetLastError</span></span>

  
  
<span data-ttu-id="ae3bf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae3bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae3bf-105">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente à l’objet de site de message en cours.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="ae3bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae3bf-106">Parameters</span></span>

 <span data-ttu-id="ae3bf-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="ae3bf-107">_hResult_</span></span>
  
> <span data-ttu-id="ae3bf-108">[in] Une valeur HRESULT qui contient la valeur d’erreur générée lors de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-108">[in] An HRESULT that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="ae3bf-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ae3bf-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ae3bf-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="ae3bf-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="ae3bf-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ae3bf-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ae3bf-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ae3bf-113">Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="ae3bf-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ae3bf-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ae3bf-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="ae3bf-116">[out] Pointeur vers un pointeur vers la structure **MAPIERROR** retournée qui contient les informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="ae3bf-117">Ce paramètre peut être défini sur la valeur NULL s’il n’existe aucune structure **MAPIERROR** pour renvoyer.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ae3bf-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae3bf-118">Return value</span></span>

<span data-ttu-id="ae3bf-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae3bf-119">S_OK</span></span>
  
> <span data-ttu-id="ae3bf-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ae3bf-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ae3bf-121">MAPI_E_BAD_CHARWIDTH</span></span>
  
> <span data-ttu-id="ae3bf-122">Soit l’indicateur MAPI_UNICODE a été défini et **GetLastError** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **GetLastError** prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ae3bf-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="ae3bf-123">Remarks</span></span>

<span data-ttu-id="ae3bf-124">La méthode **IMAPIMessageSite::GetLastError** fournit des informations sur un appel de méthode antérieurs ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-124">The **IMAPIMessageSite::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="ae3bf-125">Les appelants peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant les données à partir de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ae3bf-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="ae3bf-126">Notes to callers</span></span>

<span data-ttu-id="ae3bf-127">Vous pouvez vous servir de la **MAPIERROR** structure indiquée par le paramètre _lppMAPIError_ si MAPI fournit une uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="ae3bf-128">Parfois MAPI ne peut pas déterminer ce qui a été la dernière erreur ou n’a rien de plus de rapport sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-128">Sometimes MAPI cannot determine what the last error was, or has nothing more to report about the error.</span></span> <span data-ttu-id="ae3bf-129">Dans ce cas, un pointeur vers la valeur NULL est retourné dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="ae3bf-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="ae3bf-130">Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue à l’aide](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="ae3bf-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae3bf-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae3bf-131">See also</span></span>



[<span data-ttu-id="ae3bf-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="ae3bf-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="ae3bf-133">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae3bf-133">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)

