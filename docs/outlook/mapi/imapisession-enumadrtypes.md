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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 6bd13eb7180302a5ab770586cf36856ca5a22676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783925"
---
# <a name="imapisessionenumadrtypes"></a><span data-ttu-id="f0df1-103">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="f0df1-103">IMAPISession::EnumAdrTypes</span></span>

  
  
<span data-ttu-id="f0df1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0df1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0df1-105">Déconseillé.</span><span class="sxs-lookup"><span data-stu-id="f0df1-105">Deprecated.</span></span> <span data-ttu-id="f0df1-106">Renvoie les types d’adresses qui peuvent être gérés par tous les fournisseurs de transport dans la session.</span><span class="sxs-lookup"><span data-stu-id="f0df1-106">Returns the address types that can be handled by all of the transport providers in the session.</span></span> 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a><span data-ttu-id="f0df1-107">Param�tres</span><span class="sxs-lookup"><span data-stu-id="f0df1-107">Parameters</span></span>

 <span data-ttu-id="f0df1-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f0df1-108">_ulFlags_</span></span>
  
> <span data-ttu-id="f0df1-109">[in] Masque de bits d’indicateurs qui indique le format pour les types d’adresse retournée.</span><span class="sxs-lookup"><span data-stu-id="f0df1-109">[in] A bitmask of flags that indicates the format for the returned address types.</span></span> <span data-ttu-id="f0df1-110">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="f0df1-110">The following flag can be set:</span></span>
    
<span data-ttu-id="f0df1-111">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0df1-111">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f0df1-112">Les types d’adresses sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0df1-112">The address types are in Unicode format.</span></span> <span data-ttu-id="f0df1-113">Si l’indicateur MAPI_UNICODE n’est pas définie, les types d’adresses sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="f0df1-113">If the MAPI_UNICODE flag is not set, the address types are in ANSI format.</span></span>
    
 <span data-ttu-id="f0df1-114">_lpcAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="f0df1-114">_lpcAdrTypes_</span></span>
  
> <span data-ttu-id="f0df1-115">[out] Un pointeur vers un nombre de types d’adresses indiqué par le paramètre _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="f0df1-115">[out] A pointer to a count of address types pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
    
 <span data-ttu-id="f0df1-116">_lpppszAdrTypes_</span><span class="sxs-lookup"><span data-stu-id="f0df1-116">_lpppszAdrTypes_</span></span>
  
> <span data-ttu-id="f0df1-117">[out] Pointeur vers un tableau de pointeurs vers des types d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f0df1-117">[out] A pointer to an array of pointers to address types.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0df1-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f0df1-118">Return value</span></span>

<span data-ttu-id="f0df1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0df1-119">S_OK</span></span> 
  
> <span data-ttu-id="f0df1-120">Les types d’adresses ont été récupérés correctement.</span><span class="sxs-lookup"><span data-stu-id="f0df1-120">The address types were successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0df1-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0df1-121">Remarks</span></span>

<span data-ttu-id="f0df1-122">La méthode **IMAPISession::EnumAdrTypes** renvoie une liste des types d’adresses qui peuvent être gérés par tous les fournisseurs de transport actif dans la session.</span><span class="sxs-lookup"><span data-stu-id="f0df1-122">The **IMAPISession::EnumAdrTypes** method returns a list of the address types that can be handled by all of the active transport providers in the session.</span></span> <span data-ttu-id="f0df1-123">Les types d’adresses pour les fournisseurs de transport qui ne sont pas actuellement chargés ne sont pas inclus dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f0df1-123">The address types for transport providers that are not currently loaded are not included in the list.</span></span> <span data-ttu-id="f0df1-124">Fournisseurs de transport enregistrement pour gérer un ou plusieurs types d’adresses lors de leur méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) des appels MAPI.</span><span class="sxs-lookup"><span data-stu-id="f0df1-124">Transport providers register to handle one or more address types when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f0df1-125">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="f0df1-125">Notes to callers</span></span>

<span data-ttu-id="f0df1-126">Appelez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de chaînes désigné par le paramètre _lpppszAdrTypes_ .</span><span class="sxs-lookup"><span data-stu-id="f0df1-126">Call [MAPIFreeBuffer](mapifreebuffer.md) to release the string array pointed to by the  _lpppszAdrTypes_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0df1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0df1-127">See also</span></span>



[<span data-ttu-id="f0df1-128">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="f0df1-128">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="f0df1-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f0df1-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f0df1-130">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f0df1-130">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

