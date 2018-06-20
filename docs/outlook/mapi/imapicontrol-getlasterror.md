---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2be5e40de6894b99d9de86423e99dd95a08bc04c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783689"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="36369-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="36369-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="36369-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36369-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36369-105">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de contrôle de bouton précédent.</span><span class="sxs-lookup"><span data-stu-id="36369-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="36369-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36369-106">Parameters</span></span>

 <span data-ttu-id="36369-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="36369-107">_hResult_</span></span>
  
> <span data-ttu-id="36369-108">[in] Handle vers la valeur d’erreur généré lors de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="36369-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="36369-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36369-109">_ulFlags_</span></span>
  
> <span data-ttu-id="36369-110">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="36369-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="36369-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="36369-111">The following flag can be set:</span></span>
    
<span data-ttu-id="36369-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="36369-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="36369-113">Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="36369-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="36369-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="36369-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="36369-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="36369-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="36369-116">[out] Pointeur vers un pointeur vers une structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="36369-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="36369-117">Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL si le fournisseur ne peut pas fournir une structure **MAPIERROR** avec les informations appropriées.</span><span class="sxs-lookup"><span data-stu-id="36369-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36369-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="36369-118">Return value</span></span>

<span data-ttu-id="36369-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="36369-119">S_OK</span></span> 
  
> <span data-ttu-id="36369-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="36369-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="36369-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="36369-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="36369-122">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="36369-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36369-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="36369-123">Remarks</span></span>

<span data-ttu-id="36369-124">Fournisseurs de services implémentent la méthode **IMAPIControl::GetLastError** pour fournir des informations relatives à un appel de méthode antérieurs ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="36369-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="36369-125">MAPI peut fournir des utilisateurs des informations détaillées sur l’erreur en affichant les données à partir de la structure **MAPIERROR** dans une zone de message ou de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="36369-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="36369-126">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="36369-126">Notes to implementers</span></span>

<span data-ttu-id="36369-127">Il est inutile de disposer d’informations à inclure dans la structure **MAPIERROR** pour chaque erreur.</span><span class="sxs-lookup"><span data-stu-id="36369-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="36369-128">Il peut être pas possible de déterminer quel est l’erreur précédente.</span><span class="sxs-lookup"><span data-stu-id="36369-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="36369-129">Si vous disposez des informations, renvoie S_OK et les données appropriées dans la structure **MAPIERROR** .</span><span class="sxs-lookup"><span data-stu-id="36369-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="36369-130">Si aucune information n’est disponible, renvoie S_OK et un pointeur null pour le paramètre _lppMAPIError_ .</span><span class="sxs-lookup"><span data-stu-id="36369-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="36369-131">Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="36369-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36369-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36369-132">See also</span></span>



[<span data-ttu-id="36369-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="36369-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="36369-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="36369-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="36369-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36369-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

