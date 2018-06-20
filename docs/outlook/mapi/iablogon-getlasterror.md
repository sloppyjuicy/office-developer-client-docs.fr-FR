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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: bead72ab2b394634217c9ae219a03a98752ef27d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783581"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="e3ca1-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e3ca1-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="e3ca1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3ca1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3ca1-105">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de fournisseur livre adresse précédente.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="e3ca1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3ca1-106">Parameters</span></span>

 <span data-ttu-id="e3ca1-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="e3ca1-107">_hResult_</span></span>
  
> <span data-ttu-id="e3ca1-108">[in] Handle vers la valeur d’erreur généré lors de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="e3ca1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e3ca1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e3ca1-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="e3ca1-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="e3ca1-111">The following flag can be set:</span></span>
    
<span data-ttu-id="e3ca1-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e3ca1-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e3ca1-113">Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="e3ca1-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="e3ca1-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="e3ca1-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="e3ca1-116">[out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="e3ca1-117">Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL si le fournisseur ne peut pas fournir une structure **MAPIERROR** avec les informations appropriées.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e3ca1-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e3ca1-118">Return value</span></span>

<span data-ttu-id="e3ca1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3ca1-119">S_OK</span></span> 
  
> <span data-ttu-id="e3ca1-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e3ca1-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e3ca1-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e3ca1-122">Soit l’indicateur MAPI_UNICODE a été défini et le fournisseur de carnet d’adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et le fournisseur de carnet d’adresses prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3ca1-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3ca1-123">Remarks</span></span>

<span data-ttu-id="e3ca1-124">Fournisseurs de carnet d’adresses implémentent la méthode **GetLastError** pour fournir des informations relatives à un appel de méthode antérieurs ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="e3ca1-125">Les appelants peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant les données à partir de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e3ca1-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="e3ca1-126">Notes to callers</span></span>

<span data-ttu-id="e3ca1-127">Vous pouvez utiliser la structure **MAPIERROR** désignée par le paramètre _lppMAPIError_ si le fournisseur de carnet d’adresses fournit la structure et seulement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="e3ca1-128">Parfois, le fournisseur de carnet d’adresses ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="e3ca1-129">Dans ce cas, le fournisseur de carnet d’adresses renvoie un pointeur null dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="e3ca1-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="e3ca1-130">Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="e3ca1-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e3ca1-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3ca1-131">See also</span></span>



[<span data-ttu-id="e3ca1-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="e3ca1-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="e3ca1-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e3ca1-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e3ca1-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3ca1-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

