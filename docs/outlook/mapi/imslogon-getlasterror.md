---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425875"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="e5727-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e5727-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="e5727-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5727-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5727-105">Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur survenue pour l'objet de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e5727-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="e5727-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5727-106">Parameters</span></span>

 <span data-ttu-id="e5727-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="e5727-107">_hResult_</span></span>
  
> <span data-ttu-id="e5727-108">dans Un type de données HRESULT qui contient la valeur d'erreur générée dans l'appel de méthode précédent pour l'objet de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e5727-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="e5727-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e5727-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e5727-110">dans Masque de des indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="e5727-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="e5727-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="e5727-111">The following flag can be set:</span></span>
    
<span data-ttu-id="e5727-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e5727-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e5727-113">Les chaînes de la structure **MAPIERROR** renvoyées dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="e5727-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="e5727-114">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="e5727-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="e5727-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="e5727-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="e5727-116">remarquer Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée qui contient les informations de version, de composant et de contexte pour l'erreur.</span><span class="sxs-lookup"><span data-stu-id="e5727-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="e5727-117">Le paramètre _lppMAPIError_ peut être défini sur null s'il n'y a pas de **MAPIERROR** à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="e5727-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e5727-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e5727-118">Return value</span></span>

<span data-ttu-id="e5727-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5727-119">S_OK</span></span> 
  
> <span data-ttu-id="e5727-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e5727-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e5727-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e5727-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e5727-122">L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="e5727-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e5727-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="e5727-123">Remarks</span></span>

<span data-ttu-id="e5727-124">Utilisez la méthode **IMSLogon:: GetLastError** pour extraire les informations à afficher dans un message à l'utilisateur concernant la dernière erreur renvoyée par un appel de méthode pour l'objet de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e5727-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="e5727-125">Pour libérer toute la mémoire allouée par MAPI pour la structure **MAPIERROR** renvoyée, les applications clientes doivent appeler uniquement la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e5727-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="e5727-126">La valeur renvoyée par **GetLastError** doit être S_OK pour qu'une application utilise **MAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="e5727-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="e5727-127">Même si la valeur renvoyée est S_OK, il se peut qu'un **MAPIERROR** ne soit pas retourné.</span><span class="sxs-lookup"><span data-stu-id="e5727-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="e5727-128">Si l'implémentation ne peut pas déterminer la dernière erreur ou si un **MAPIERROR** n'est pas disponible pour cette erreur, **GetLastError** renvoie un pointeur vers une valeur null dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="e5727-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e5727-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5727-129">See also</span></span>



[<span data-ttu-id="e5727-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="e5727-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="e5727-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e5727-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e5727-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5727-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

