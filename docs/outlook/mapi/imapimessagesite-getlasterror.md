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
ms.openlocfilehash: cc4de8aa21d4b3b27bf757389b663ebeff69a9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420737"
---
# <a name="imapimessagesitegetlasterror"></a><span data-ttu-id="c82cc-103">IMAPIMessageSite::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c82cc-103">IMAPIMessageSite::GetLastError</span></span>

  
  
<span data-ttu-id="c82cc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c82cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c82cc-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente qui s’est produite sur l’objet de site de message.</span><span class="sxs-lookup"><span data-stu-id="c82cc-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="c82cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c82cc-106">Parameters</span></span>

 <span data-ttu-id="c82cc-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="c82cc-107">_hResult_</span></span>
  
> <span data-ttu-id="c82cc-108">[in] Valeur HRESULT qui contient la valeur d’erreur générée dans l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="c82cc-108">[in] An HRESULT that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="c82cc-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c82cc-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c82cc-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="c82cc-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="c82cc-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="c82cc-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c82cc-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c82cc-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c82cc-113">Les chaînes de la structure **MAPIERROR renvoyées** dans le paramètre  _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="c82cc-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="c82cc-114">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="c82cc-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="c82cc-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c82cc-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="c82cc-116">[out] Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée qui contient les informations de version, de composant et de contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c82cc-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="c82cc-117">Ce paramètre peut être définie sur NULL s’il n’existe aucune structure **MAPIERROR** à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="c82cc-117">This parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c82cc-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c82cc-118">Return value</span></span>

<span data-ttu-id="c82cc-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c82cc-119">S_OK</span></span>
  
> <span data-ttu-id="c82cc-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c82cc-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c82cc-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c82cc-121">MAPI_E_BAD_CHARWIDTH</span></span>
  
> <span data-ttu-id="c82cc-122">L’MAPI_UNICODE a été définie et **GetLastError** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **GetLastError** prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="c82cc-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c82cc-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="c82cc-123">Remarks</span></span>

<span data-ttu-id="c82cc-124">La **méthode IMAPIMessageSite::GetLastError** fournit des informations sur un appel de méthode antérieur qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="c82cc-124">The **IMAPIMessageSite::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="c82cc-125">Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c82cc-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c82cc-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="c82cc-126">Notes to callers</span></span>

<span data-ttu-id="c82cc-127">Vous pouvez utiliser la structure **MAPIERROR** pointée par le paramètre  _lppMAPIError_ si MAPI en fournit un uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="c82cc-127">You can make use of the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if MAPI supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="c82cc-128">Parfois, MAPI ne peut pas déterminer la dernière erreur ou n’a rien d’autre à signaler à propos de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c82cc-128">Sometimes MAPI cannot determine what the last error was, or has nothing more to report about the error.</span></span> <span data-ttu-id="c82cc-129">Dans ce cas, un pointeur vers NULL est renvoyé dans  _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="c82cc-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="c82cc-130">Pour plus d’informations **sur la méthode GetLastError,** voir [Using Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c82cc-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c82cc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c82cc-131">See also</span></span>



[<span data-ttu-id="c82cc-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c82cc-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c82cc-133">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c82cc-133">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)

