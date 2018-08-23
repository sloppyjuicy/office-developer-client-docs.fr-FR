---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 34de52693d8484abb28d2ee2f7b86f15e8bd037b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574102"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="70de9-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="70de9-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="70de9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70de9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70de9-105">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de session précédente.</span><span class="sxs-lookup"><span data-stu-id="70de9-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="70de9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70de9-106">Parameters</span></span>

 <span data-ttu-id="70de9-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="70de9-107">_hResult_</span></span>
  
> <span data-ttu-id="70de9-108">[in] Handle vers la valeur d’erreur généré lors de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="70de9-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="70de9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="70de9-109">_ulFlags_</span></span>
  
> <span data-ttu-id="70de9-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="70de9-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="70de9-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="70de9-111">The following flag can be set:</span></span>
    
<span data-ttu-id="70de9-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="70de9-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="70de9-113">Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="70de9-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="70de9-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="70de9-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="70de9-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="70de9-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="70de9-116">[out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="70de9-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="70de9-117">Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL si MAPI ne peut pas fournir les informations appropriées pour une structure **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="70de9-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="70de9-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="70de9-118">Return value</span></span>

<span data-ttu-id="70de9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="70de9-119">S_OK</span></span> 
  
> <span data-ttu-id="70de9-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="70de9-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="70de9-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="70de9-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="70de9-122">L’indicateur MAPI_UNICODE a été défini et que la session ne prend pas en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="70de9-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70de9-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="70de9-123">Remarks</span></span>

<span data-ttu-id="70de9-124">La méthode **IMAPISession::GetLastError** récupère des informations sur la dernière erreur a été renvoyée par un appel de la méthode **IMAPISession** .</span><span class="sxs-lookup"><span data-stu-id="70de9-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="70de9-125">Les clients peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant ces informations dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="70de9-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="70de9-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="70de9-126">Notes to callers</span></span>

<span data-ttu-id="70de9-127">Vous pouvez utiliser la structure **MAPIERROR** , si MAPI en fournit une, désignés par if seul paramètre _lppMAPIError_ **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="70de9-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="70de9-128">Parfois MAPI ne peut pas déterminer quelle était la dernière erreur, ou il a rien de plus de rapport sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="70de9-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="70de9-129">Dans ce cas, **GetLastError** retourne un pointeur null dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="70de9-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="70de9-130">Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="70de9-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="70de9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70de9-131">See also</span></span>



[<span data-ttu-id="70de9-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="70de9-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="70de9-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="70de9-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="70de9-134">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="70de9-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="70de9-135">MAPI �tendue des erreurs</span><span class="sxs-lookup"><span data-stu-id="70de9-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

