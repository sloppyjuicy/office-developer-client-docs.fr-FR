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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a865a751f3e274008c7004315906d6705ba55161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784313"
---
# <a name="imslogongetlasterror"></a><span data-ttu-id="8658f-103">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8658f-103">IMSLogon::GetLastError</span></span>

  
  
<span data-ttu-id="8658f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8658f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8658f-105">Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur la dernière erreur qui s’est produite lors de l’objet de la banque de message.</span><span class="sxs-lookup"><span data-stu-id="8658f-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="8658f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8658f-106">Parameters</span></span>

 <span data-ttu-id="8658f-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="8658f-107">_hResult_</span></span>
  
> <span data-ttu-id="8658f-108">[in] Un type de données HRESULT qui contient la valeur d’erreur générée dans l’appel de méthode précédent pour l’objet de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8658f-108">[in] An HRESULT data type that contains the error value generated in the previous method call for the message store object.</span></span>
    
 <span data-ttu-id="8658f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8658f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8658f-110">[in] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="8658f-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="8658f-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="8658f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="8658f-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8658f-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8658f-113">Les chaînes dans la structure **MAPIERROR** retournée dans le paramètre _lppMAPIError_ sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="8658f-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="8658f-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="8658f-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="8658f-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="8658f-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="8658f-116">[out] Pointeur vers un pointeur vers la structure **MAPIERROR** retournée qui contient les informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="8658f-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="8658f-117">Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucun **MAPIERROR** pour renvoyer.</span><span class="sxs-lookup"><span data-stu-id="8658f-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8658f-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8658f-118">Return value</span></span>

<span data-ttu-id="8658f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8658f-119">S_OK</span></span> 
  
> <span data-ttu-id="8658f-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="8658f-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="8658f-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8658f-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8658f-122">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="8658f-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8658f-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="8658f-123">Remarks</span></span>

<span data-ttu-id="8658f-124">Utilisez la méthode **IMSLogon::GetLastError** pour récupérer des informations à afficher dans un message à l’utilisateur concernant la dernière erreur renvoyée par un appel de méthode pour l’objet de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8658f-124">Use the **IMSLogon::GetLastError** method to retrieve information to display in a message to the user regarding the last error returned from a method call for the message store object.</span></span> 
  
<span data-ttu-id="8658f-125">Pour libérer la mémoire allouée par MAPI pour la structure **MAPIERROR** retournée, les applications clientes ont besoin d’appeler la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement.</span><span class="sxs-lookup"><span data-stu-id="8658f-125">To release all the memory allocated by MAPI for the returned **MAPIERROR** structure, client applications need to call only the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="8658f-126">La valeur renvoyée par **GetLastError** doit être S_OK d’une application pour utiliser le **MAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="8658f-126">The return value from **GetLastError** must be S_OK for an application to use the **MAPIERROR**.</span></span> <span data-ttu-id="8658f-127">Même si la valeur de retour est S_OK, un **MAPIERROR** ne peut pas être retourné.</span><span class="sxs-lookup"><span data-stu-id="8658f-127">Even if the return value is S_OK, a **MAPIERROR** might not be returned.</span></span> <span data-ttu-id="8658f-128">Si l’implémentation ne peut pas déterminer quelle était la dernière erreur, ou si une **MAPIERROR** n’est pas disponible pour que l’erreur, **GetLastError** retourne un pointeur vers NULL dans _lppMAPIError_ à la place.</span><span class="sxs-lookup"><span data-stu-id="8658f-128">If the implementation cannot determine what the last error was, or if a **MAPIERROR** is not available for that error, **GetLastError** returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8658f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8658f-129">See also</span></span>



[<span data-ttu-id="8658f-130">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="8658f-130">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="8658f-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8658f-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8658f-132">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8658f-132">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

