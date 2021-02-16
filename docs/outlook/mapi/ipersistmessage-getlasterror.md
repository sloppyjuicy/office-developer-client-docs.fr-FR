---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426708"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="71339-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="71339-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="71339-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71339-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71339-105">Renvoie une [structure MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente dans l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="71339-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="71339-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71339-106">Parameters</span></span>

 <span data-ttu-id="71339-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="71339-107">_hResult_</span></span>
  
> <span data-ttu-id="71339-108">[in] Type de données HRESULT qui contient la valeur d’erreur générée dans l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="71339-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="71339-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="71339-109">_ulFlags_</span></span>
  
> <span data-ttu-id="71339-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="71339-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="71339-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="71339-111">The following flag can be set:</span></span>
    
<span data-ttu-id="71339-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="71339-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="71339-113">Les chaînes de la structure [MAPIERROR renvoyées](mapierror.md) dans le paramètre  _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="71339-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="71339-114">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="71339-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="71339-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="71339-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="71339-116">[out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, de composant et de contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="71339-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="71339-117">Le _paramètre lppMAPIError_ peut avoir la valeur NULL si le formulaire ne peut pas fournir les informations appropriées pour une structure **MAPIERROR.**</span><span class="sxs-lookup"><span data-stu-id="71339-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="71339-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71339-118">Return value</span></span>

<span data-ttu-id="71339-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="71339-119">S_OK</span></span> 
  
> <span data-ttu-id="71339-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="71339-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="71339-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="71339-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="71339-122">L’indicateur MAPI_UNICODE a été définie et le fournisseur de carnet d’adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et le fournisseur de carnet d’adresses prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="71339-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="71339-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="71339-123">Remarks</span></span>

<span data-ttu-id="71339-124">Les objets Form implémentent la méthode **IPersistMessage::GetLastError** pour fournir des informations sur un appel de méthode antérieur qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="71339-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="71339-125">Les visionneuses de formulaires peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant les données de la structure [MAPIERROR](mapierror.md) dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="71339-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="71339-126">Un appel à **GetLastError** n’affecte pas l’état du formulaire.</span><span class="sxs-lookup"><span data-stu-id="71339-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="71339-127">Lorsque **GetLastError** est de retour, le formulaire reste dans l’état où il se trouvait avant que l’appel ne soit effectué.</span><span class="sxs-lookup"><span data-stu-id="71339-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="71339-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="71339-128">Notes to callers</span></span>

<span data-ttu-id="71339-129">Vous pouvez utiliser la structure **MAPIERROR,** si le formulaire en fournit une, qui est pointée par le paramètre  _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="71339-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="71339-130">Parfois, le formulaire ne peut pas déterminer la dernière erreur ou n’a rien d’autre à signaler à propos de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="71339-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="71339-131">Dans ce cas, le formulaire renvoie un pointeur vers NULL dans  _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="71339-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="71339-132">Pour plus d’informations **sur la méthode GetLastError,** voir [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="71339-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="71339-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71339-133">See also</span></span>



[<span data-ttu-id="71339-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="71339-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="71339-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="71339-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="71339-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="71339-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

