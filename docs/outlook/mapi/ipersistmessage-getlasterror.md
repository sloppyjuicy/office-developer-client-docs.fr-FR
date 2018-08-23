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
ms.openlocfilehash: a39deb57a24b3a89ee10020a6442bcb1bca612a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575307"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="c0f83-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c0f83-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="c0f83-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0f83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0f83-105">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente dans l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="c0f83-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="c0f83-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0f83-106">Parameters</span></span>

 <span data-ttu-id="c0f83-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="c0f83-107">_hResult_</span></span>
  
> <span data-ttu-id="c0f83-108">[in] Un type de données HRESULT qui contient la valeur d’erreur générée lors de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="c0f83-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="c0f83-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0f83-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c0f83-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="c0f83-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="c0f83-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="c0f83-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c0f83-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c0f83-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c0f83-113">Les chaînes dans la structure [MAPIERROR](mapierror.md) retournée dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="c0f83-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="c0f83-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="c0f83-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="c0f83-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c0f83-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="c0f83-116">[out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c0f83-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="c0f83-117">Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL si le formulaire ne peut pas fournir les informations appropriées pour une structure **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="c0f83-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c0f83-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c0f83-118">Return value</span></span>

<span data-ttu-id="c0f83-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0f83-119">S_OK</span></span> 
  
> <span data-ttu-id="c0f83-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c0f83-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c0f83-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c0f83-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c0f83-122">Soit l’indicateur MAPI_UNICODE a été défini et le fournisseur de carnet d’adresses ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et le fournisseur de carnet d’adresses prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="c0f83-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0f83-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0f83-123">Remarks</span></span>

<span data-ttu-id="c0f83-124">Objets de formulaire implémentent la méthode de **IPersistMessage::GetLastError** pour fournir des informations relatives à un appel de méthode antérieurs ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="c0f83-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="c0f83-125">Visionneuses de formulaire peuvent fournir à leurs utilisateurs des informations détaillées sur l’erreur en incluant les données à partir de la structure [MAPIERROR](mapierror.md) dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c0f83-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="c0f83-126">Un appel à **GetLastError** n’affecte pas l’état du formulaire.</span><span class="sxs-lookup"><span data-stu-id="c0f83-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="c0f83-127">**GetLastError** retourne le formulaire reste dans l’état dans lequel elle se trouvait avant l’appel a été effectué.</span><span class="sxs-lookup"><span data-stu-id="c0f83-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c0f83-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="c0f83-128">Notes to callers</span></span>

<span data-ttu-id="c0f83-129">Vous pouvez utiliser la structure **MAPIERROR** , si le formulaire fournit une, ce qui est indiqué par le paramètre _lppMAPIError_ uniquement si **GetLastError** renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="c0f83-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="c0f83-130">Parfois, le formulaire ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c0f83-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="c0f83-131">Dans ce cas, le formulaire retourne un pointeur null dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="c0f83-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="c0f83-132">Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c0f83-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0f83-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0f83-133">See also</span></span>



[<span data-ttu-id="c0f83-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c0f83-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c0f83-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c0f83-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c0f83-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0f83-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

