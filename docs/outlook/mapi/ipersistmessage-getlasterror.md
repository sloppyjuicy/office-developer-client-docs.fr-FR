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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317163"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="af6b7-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="af6b7-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="af6b7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af6b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af6b7-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur précédente dans l'objet Form.</span><span class="sxs-lookup"><span data-stu-id="af6b7-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="af6b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af6b7-106">Parameters</span></span>

 <span data-ttu-id="af6b7-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="af6b7-107">_hResult_</span></span>
  
> <span data-ttu-id="af6b7-108">dans Un type de données HRESULT qui contient la valeur d'erreur générée lors de l'appel de la méthode précédente.</span><span class="sxs-lookup"><span data-stu-id="af6b7-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="af6b7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af6b7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="af6b7-110">dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="af6b7-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="af6b7-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="af6b7-111">The following flag can be set:</span></span>
    
<span data-ttu-id="af6b7-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af6b7-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="af6b7-113">Les chaînes de la structure [MAPIERROR](mapierror.md) renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="af6b7-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="af6b7-114">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="af6b7-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="af6b7-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="af6b7-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="af6b7-116">remarquer Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, de composant et de contexte pour l'erreur.</span><span class="sxs-lookup"><span data-stu-id="af6b7-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="af6b7-117">Le paramètre _lppMAPIError_ peut être défini sur null si le formulaire ne peut pas fournir les informations appropriées pour une structure **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="af6b7-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="af6b7-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="af6b7-118">Return value</span></span>

<span data-ttu-id="af6b7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="af6b7-119">S_OK</span></span> 
  
> <span data-ttu-id="af6b7-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="af6b7-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="af6b7-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="af6b7-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="af6b7-122">L'indicateur MAPI_UNICODE a été défini et le fournisseur de carnet d'adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et le fournisseur de carnet d'adresses prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="af6b7-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af6b7-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="af6b7-123">Remarks</span></span>

<span data-ttu-id="af6b7-124">Les objets Form implémentent la méthode **IPersistMessage:: GetLastError** pour fournir des informations sur un appel de méthode précédent qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="af6b7-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="af6b7-125">Les visionneuses de formulaires peuvent fournir à leurs utilisateurs des informations détaillées sur l'erreur en incluant les données de la structure [MAPIERROR](mapierror.md) dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="af6b7-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="af6b7-126">Un appel à **GetLastError** n'affecte pas l'état du formulaire.</span><span class="sxs-lookup"><span data-stu-id="af6b7-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="af6b7-127">Lorsque **GetLastError** est renvoyé, le formulaire reste à l'État dans lequel il se trouvait avant la création de l'appel.</span><span class="sxs-lookup"><span data-stu-id="af6b7-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="af6b7-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="af6b7-128">Notes to callers</span></span>

<span data-ttu-id="af6b7-129">Vous pouvez utiliser la structure **MAPIERROR** , si le formulaire en fournit un, pointant par le paramètre _LppMAPIError_ uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="af6b7-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="af6b7-130">Parfois, le formulaire ne peut pas déterminer la dernière erreur ou n'a rien de plus à signaler à propos de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="af6b7-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="af6b7-131">Dans ce cas, le formulaire renvoie un pointeur vers une valeur NULL dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="af6b7-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="af6b7-132">Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [erreurs étendues MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="af6b7-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af6b7-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af6b7-133">See also</span></span>



[<span data-ttu-id="af6b7-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="af6b7-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="af6b7-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="af6b7-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="af6b7-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af6b7-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

