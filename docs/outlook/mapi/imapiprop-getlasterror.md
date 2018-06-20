---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 67aa5b3d85de3df659b5aa1a351ec0d1dcf90248
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783896"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="7e6df-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7e6df-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="7e6df-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e6df-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e6df-105">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente.</span><span class="sxs-lookup"><span data-stu-id="7e6df-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="7e6df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e6df-106">Parameters</span></span>

 <span data-ttu-id="7e6df-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="7e6df-107">_hResult_</span></span>
  
> <span data-ttu-id="7e6df-108">[in] Handle vers le code d’erreur généré lors de l’appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="7e6df-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="7e6df-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e6df-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7e6df-110">[in] Masque de bits d’indicateurs qui indique le format du texte retourné dans la structure **MAPIERROR** désignée par _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="7e6df-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="7e6df-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="7e6df-111">The following flag can be set:</span></span>
    
<span data-ttu-id="7e6df-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7e6df-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7e6df-113">Les chaînes doivent être au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e6df-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="7e6df-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes doivent être au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="7e6df-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="7e6df-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="7e6df-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="7e6df-116">[out] Pointeur vers un pointeur vers la structure **MAPIERROR** qui contient les informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="7e6df-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="7e6df-117">Le paramètre _lppMAPIError_ peut être défini sur NULL s’il n’existe aucune information d’erreur à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="7e6df-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7e6df-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="7e6df-118">Return value</span></span>

<span data-ttu-id="7e6df-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e6df-119">S_OK</span></span> 
  
> <span data-ttu-id="7e6df-120">Les informations d’erreur a été renvoyées.</span><span class="sxs-lookup"><span data-stu-id="7e6df-120">The error information was returned.</span></span>
    
<span data-ttu-id="7e6df-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7e6df-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7e6df-122">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="7e6df-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e6df-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="7e6df-123">Remarks</span></span>

<span data-ttu-id="7e6df-124">La méthode **IMAPIProp::GetLastError** fournit des informations sur un appel de méthode antérieurs ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="7e6df-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="7e6df-125">Les clients peuvent fournir leurs utilisateurs avec des informations détaillées sur l’erreur en incluant les données à partir de la structure **MAPIERROR** dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7e6df-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="7e6df-126">Toutes les implémentations de **GetLastError** fourni par MAPI sont mises en œuvre ANSI, à l’exception de l’implémentation de [IAddrBook](iaddrbookimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="7e6df-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="7e6df-127">La méthode **GetLastError** incluse avec **IAddrBook** prend en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e6df-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7e6df-128">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="7e6df-128">Notes to implementers</span></span>

<span data-ttu-id="7e6df-129">Les détails d’une distance de transport du fournisseur d’implémentation de cette méthode et quels sont les messages, que cette méthode retourne le fournisseur de transport, étant donné que les conditions d’erreur spécifique qui mènent à des différentes valeurs HRESULT sera différentes pour le transport différents fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="7e6df-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7e6df-130">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="7e6df-130">Notes to callers</span></span>

<span data-ttu-id="7e6df-131">Vous pouvez utiliser la structure **MAPIERROR** désignée par le paramètre _lppMAPIError_ , si **GetLastError** fournit un, uniquement si la valeur renvoyée est S_OK.</span><span class="sxs-lookup"><span data-stu-id="7e6df-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="7e6df-132">Il est parfois **GetLastError** ne peut pas déterminer la dernière erreur a été ou n’a rien de plus de rapport sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="7e6df-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="7e6df-133">Dans ce cas, un pointeur vers la valeur NULL est retourné dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="7e6df-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="7e6df-134">Pour libérer de la mémoire pour la structure **MAPIERROR** , appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7e6df-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="7e6df-135">Pour plus d’informations sur la méthode **GetLastError** , voir [Erreurs d’étendue MAPI](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="7e6df-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e6df-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e6df-136">See also</span></span>



[<span data-ttu-id="7e6df-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7e6df-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="7e6df-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="7e6df-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="7e6df-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7e6df-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7e6df-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e6df-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="7e6df-141">MAPI étendue des erreurs</span><span class="sxs-lookup"><span data-stu-id="7e6df-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

