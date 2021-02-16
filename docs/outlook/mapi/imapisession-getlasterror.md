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
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435578"
---
# <a name="imapisessiongetlasterror"></a><span data-ttu-id="12372-103">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="12372-103">IMAPISession::GetLastError</span></span>

  
  
<span data-ttu-id="12372-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12372-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12372-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de session précédente.</span><span class="sxs-lookup"><span data-stu-id="12372-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="12372-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12372-106">Parameters</span></span>

 <span data-ttu-id="12372-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="12372-107">_hResult_</span></span>
  
> <span data-ttu-id="12372-108">[in] Handle vers la valeur d’erreur générée dans l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="12372-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="12372-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="12372-109">_ulFlags_</span></span>
  
> <span data-ttu-id="12372-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="12372-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="12372-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="12372-111">The following flag can be set:</span></span>
    
<span data-ttu-id="12372-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="12372-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="12372-113">Les chaînes de la structure **MAPIERROR renvoyées** dans le paramètre  _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="12372-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="12372-114">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="12372-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="12372-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="12372-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="12372-116">[out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, de composant et de contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="12372-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="12372-117">Le _paramètre lppMAPIError_ peut avoir la valeur NULL si MAPI ne peut pas fournir les informations appropriées pour une structure **MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="12372-117">The  _lppMAPIError_ parameter can be set to NULL if MAPI cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="12372-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="12372-118">Return value</span></span>

<span data-ttu-id="12372-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="12372-119">S_OK</span></span> 
  
> <span data-ttu-id="12372-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="12372-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="12372-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="12372-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="12372-122">L’MAPI_UNICODE a été définie et la session ne prend pas en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="12372-122">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12372-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="12372-123">Remarks</span></span>

<span data-ttu-id="12372-124">La **méthode IMAPISession::GetLastError** récupère des informations sur la dernière erreur renvoyée par un appel de méthode **IMAPISession.**</span><span class="sxs-lookup"><span data-stu-id="12372-124">The **IMAPISession::GetLastError** method retrieves information about the last error that was returned by an **IMAPISession** method call.</span></span> <span data-ttu-id="12372-125">Les clients peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant ces informations dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="12372-125">Clients can provide their users with detailed information about the error by including this information in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="12372-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="12372-126">Notes to callers</span></span>

<span data-ttu-id="12372-127">Vous pouvez utiliser la structure **MAPIERROR,** si MAPI en fournit un, pointée par le paramètre  _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="12372-127">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="12372-128">Parfois, MAPI ne peut pas déterminer la dernière erreur, ou il n’a rien d’autre à signaler à propos de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="12372-128">Sometimes MAPI cannot determine what the last error was, or it has nothing more to report about the error.</span></span> <span data-ttu-id="12372-129">Dans ce cas, **GetLastError** renvoie un pointeur vers NULL dans  _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="12372-129">In this situation, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="12372-130">Pour plus d’informations **sur la méthode GetLastError,** voir [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="12372-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12372-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12372-131">See also</span></span>



[<span data-ttu-id="12372-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="12372-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="12372-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="12372-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="12372-134">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12372-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="12372-135">Erreurs étendues MAPI</span><span class="sxs-lookup"><span data-stu-id="12372-135">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

