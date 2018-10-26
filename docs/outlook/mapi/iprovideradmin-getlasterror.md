---
title: IProviderAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetLastError
api_type:
- COM
ms.assetid: 853ddee5-24d6-423d-b483-6a07a12de51f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 63ddf6fd8f61834c7a7faa910f70bfd98715a703
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591323"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="9a91b-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9a91b-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="9a91b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a91b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a91b-105">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente s’est produite à l’objet de l’administration du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9a91b-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="9a91b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a91b-106">Parameters</span></span>

 <span data-ttu-id="9a91b-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="9a91b-107">_hResult_</span></span>
  
> <span data-ttu-id="9a91b-108">[in] Un type de données HRESULT qui contient la valeur d’erreur générée lors de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="9a91b-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="9a91b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9a91b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9a91b-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="9a91b-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="9a91b-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="9a91b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9a91b-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9a91b-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9a91b-113">Les chaînes dans la **MAPIERROR** renvoyée dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a91b-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="9a91b-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="9a91b-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="9a91b-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="9a91b-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="9a91b-116">[out] Pointeur vers un pointeur vers la structure **MAPIERROR** retournée qui contient les informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="9a91b-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="9a91b-117">Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucun **MAPIERROR** pour renvoyer.</span><span class="sxs-lookup"><span data-stu-id="9a91b-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9a91b-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a91b-118">Return value</span></span>

<span data-ttu-id="9a91b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a91b-119">S_OK</span></span> 
  
> <span data-ttu-id="9a91b-120">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="9a91b-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="9a91b-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9a91b-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9a91b-122">Soit l’indicateur MAPI_UNICODE a été défini et **GetLastError** ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et **GetLastError** prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="9a91b-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9a91b-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a91b-123">Remarks</span></span>

<span data-ttu-id="9a91b-124">La méthode **IProviderAdmin::GetLastError** fournit des informations sur un appel de méthode antérieurs ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="9a91b-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="9a91b-125">Les appelants peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant les données à partir de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="9a91b-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9a91b-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="9a91b-126">Notes to callers</span></span>

<span data-ttu-id="9a91b-127">Vous pouvez utiliser la structure **MAPIERROR** , si MAPI fournit, que le paramètre _lppMAPIError_ pointe vers uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="9a91b-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="9a91b-128">Il est parfois MAPI ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="9a91b-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="9a91b-129">Dans ce cas, un pointeur vers la valeur NULL est retourné dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="9a91b-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="9a91b-130">Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue à l’aide](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="9a91b-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a91b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a91b-131">See also</span></span>



[<span data-ttu-id="9a91b-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="9a91b-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="9a91b-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9a91b-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9a91b-134">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a91b-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

