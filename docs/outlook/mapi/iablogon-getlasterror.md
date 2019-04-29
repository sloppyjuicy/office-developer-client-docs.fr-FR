---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434248"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="40611-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="40611-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="40611-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40611-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40611-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l'erreur du fournisseur de carnet d'adresses précédent.</span><span class="sxs-lookup"><span data-stu-id="40611-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="40611-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40611-106">Parameters</span></span>

 <span data-ttu-id="40611-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="40611-107">_hResult_</span></span>
  
> <span data-ttu-id="40611-108">dans Handle de la valeur d'erreur générée lors de l'appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="40611-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="40611-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="40611-109">_ulFlags_</span></span>
  
> <span data-ttu-id="40611-110">dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="40611-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="40611-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="40611-111">The following flag can be set:</span></span>
    
<span data-ttu-id="40611-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="40611-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="40611-113">Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="40611-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="40611-114">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="40611-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="40611-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="40611-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="40611-116">remarquer Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, de composant et de contexte pour l'erreur.</span><span class="sxs-lookup"><span data-stu-id="40611-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="40611-117">Le paramètre _lppMAPIError_ peut être défini sur null si le fournisseur ne peut pas fournir une structure **MAPIERROR** avec les informations appropriées.</span><span class="sxs-lookup"><span data-stu-id="40611-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="40611-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="40611-118">Return value</span></span>

<span data-ttu-id="40611-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="40611-119">S_OK</span></span> 
  
> <span data-ttu-id="40611-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="40611-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="40611-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="40611-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="40611-122">L'indicateur MAPI_UNICODE a été défini et le fournisseur de carnet d'adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et le fournisseur de carnet d'adresses prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="40611-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40611-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="40611-123">Remarks</span></span>

<span data-ttu-id="40611-124">Les fournisseurs de carnets d'adresses implémentent la méthode **GetLastError** pour fournir des informations sur un appel de méthode précédent qui a échoué.</span><span class="sxs-lookup"><span data-stu-id="40611-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="40611-125">Les appelants peuvent fournir à leurs utilisateurs des informations détaillées sur l'erreur en incluant les données de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="40611-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="40611-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="40611-126">Notes to callers</span></span>

<span data-ttu-id="40611-127">Vous pouvez utiliser la structure **MAPIERROR** vers laquelle pointe le paramètre _lppMAPIError_ si le fournisseur de carnet d'adresses fournit la structure et uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="40611-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="40611-128">Parfois, le fournisseur de carnets d'adresses ne peut pas déterminer la dernière erreur ou n'a rien de plus à signaler à propos de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="40611-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="40611-129">Dans ce cas, le fournisseur de carnet d'adresses renvoie un pointeur vers une valeur NULL dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="40611-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="40611-130">Pour plus d'informations sur la méthode **GetLastError** , consultez la rubrique [erreurs étendues MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="40611-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40611-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40611-131">See also</span></span>



[<span data-ttu-id="40611-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="40611-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="40611-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="40611-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="40611-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40611-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

