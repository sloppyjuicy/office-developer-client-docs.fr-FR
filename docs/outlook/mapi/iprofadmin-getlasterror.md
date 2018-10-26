---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 65bf7debcae1367ccad9e109242fd4a72839a94e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584925"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="be129-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="be129-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="be129-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be129-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be129-105">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente s’est produite pour un objet d’administration de profil.</span><span class="sxs-lookup"><span data-stu-id="be129-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="be129-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be129-106">Parameters</span></span>

 <span data-ttu-id="be129-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="be129-107">_hResult_</span></span>
  
> <span data-ttu-id="be129-108">[in] Un type de données HRESULT qui contient la valeur d’erreur générée lors de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="be129-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="be129-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="be129-109">_ulFlags_</span></span>
  
> <span data-ttu-id="be129-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="be129-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="be129-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="be129-111">The following flag can be set:</span></span>
    
<span data-ttu-id="be129-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be129-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="be129-113">Les chaînes dans la structure [MAPIERROR](mapierror.md) retournée dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="be129-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="be129-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="be129-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="be129-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="be129-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="be129-116">[out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="be129-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="be129-117">Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucune structure **MAPIERROR** pour renvoyer.</span><span class="sxs-lookup"><span data-stu-id="be129-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="be129-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="be129-118">Return value</span></span>

<span data-ttu-id="be129-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="be129-119">S_OK</span></span> 
  
> <span data-ttu-id="be129-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="be129-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="be129-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="be129-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="be129-122">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="be129-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be129-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="be129-123">Remarks</span></span>

<span data-ttu-id="be129-124">La méthode **IProfAdmin::GetLastError** récupère des informations sur la dernière erreur renvoyée par un appel de méthode de l’objet d’administration de profil.</span><span class="sxs-lookup"><span data-stu-id="be129-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="be129-125">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="be129-125">Notes to callers</span></span>

<span data-ttu-id="be129-126">Vous pouvez utiliser la structure **MAPIERROR** , si MAPI en fournit une, désignés par if seul paramètre _lppMAPIError_ **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="be129-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="be129-127">Il est parfois MAPI ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="be129-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="be129-128">Dans ce cas, un pointeur vers la valeur NULL est retourné dans _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="be129-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="be129-129">Pour libérer la mémoire allouée par MAPI pour la structure **MAPIERROR** , appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="be129-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="be129-130">Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue à l’aide](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="be129-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be129-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be129-131">See also</span></span>



[<span data-ttu-id="be129-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="be129-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="be129-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="be129-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="be129-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="be129-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

