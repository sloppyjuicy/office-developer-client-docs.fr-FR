---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338436"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="79c72-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="79c72-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="79c72-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79c72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79c72-105">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="79c72-105">Deprecated.</span></span> <span data-ttu-id="79c72-106">Renvoie les types d'adresses qui peuvent être gérées par tous les fournisseurs de transport dans la session.</span><span class="sxs-lookup"><span data-stu-id="79c72-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="79c72-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79c72-107">Parameters</span></span>

 <span data-ttu-id="79c72-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="79c72-108">_ulFlags_</span></span>
  
> <span data-ttu-id="79c72-109">dans Masque de réindicateur qui indique le format des types d'adresses renvoyées.</span><span class="sxs-lookup"><span data-stu-id="79c72-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="79c72-110">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="79c72-110">The following flag can be set:</span></span>
    
<span data-ttu-id="79c72-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="79c72-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="79c72-112">Les types d'adresses sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="79c72-112">The address types are in Unicode format.</span></span> <span data-ttu-id="79c72-113">Si l'indicateur MAPI_UNICODE n'est pas défini, les types d'adresses sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="79c72-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="79c72-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="79c72-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="79c72-115">remarquer Pointeur vers le nombre de types d'adresses vers lequel pointe le paramètre _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="79c72-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="79c72-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="79c72-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="79c72-117">remarquer Pointeur vers un tableau de pointeurs vers des types d'adresses.</span><span class="sxs-lookup"><span data-stu-id="79c72-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79c72-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="79c72-118">Return value</span></span>

<span data-ttu-id="79c72-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="79c72-119">S_OK</span></span> 
  
> <span data-ttu-id="79c72-120">Les types d'adresses ont été récupérés avec succès.</span><span class="sxs-lookup"><span data-stu-id="79c72-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79c72-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="79c72-121">Remarks</span></span>

<span data-ttu-id="79c72-122">La méthode **IMAPISession:: EnumAdrTypes** renvoie la liste des types d'adresses qui peuvent être gérées par tous les fournisseurs de transport actifs dans la session.</span><span class="sxs-lookup"><span data-stu-id="79c72-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="79c72-123">Les types d'adresses pour les fournisseurs de transport qui ne sont pas actuellement chargés ne sont pas inclus dans la liste.</span><span class="sxs-lookup"><span data-stu-id="79c72-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="79c72-124">Les fournisseurs de transport s'inscrivent pour gérer un ou plusieurs types d'adresses lorsque MAPI appelle la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="79c72-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="79c72-125">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="79c72-125">Notes to callers</span></span>

<span data-ttu-id="79c72-126">Appelez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de chaînes désigné par le paramètre _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="79c72-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79c72-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79c72-127">See also</span></span>



[<span data-ttu-id="79c72-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="79c72-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="79c72-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="79c72-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="79c72-130">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79c72-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

