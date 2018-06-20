---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Crée un objet qui peut accéder à un client dans un format de caractère par défaut.
ms.openlocfilehash: 187bcbce8fd1170e05f57c5c9147a8962669fea4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782565"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="03186-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="03186-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="03186-104">Crée un objet qui peut accéder à un client dans un format de caractère par défaut.</span><span class="sxs-lookup"><span data-stu-id="03186-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="03186-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="03186-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03186-106">Exportés par :</span><span class="sxs-lookup"><span data-stu-id="03186-106">Exported by:</span></span>  <br/> |<span data-ttu-id="03186-107">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="03186-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="03186-108">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="03186-108">Called by:</span></span>  <br/> |<span data-ttu-id="03186-109">Client</span><span class="sxs-lookup"><span data-stu-id="03186-109">Client</span></span>  <br/> |
|<span data-ttu-id="03186-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="03186-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="03186-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="03186-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a><span data-ttu-id="03186-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03186-112">Parameters</span></span>

<span data-ttu-id="03186-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="03186-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="03186-114">[in] L’objet Outlook non initiale.</span><span class="sxs-lookup"><span data-stu-id="03186-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="03186-115">Doit implémenter une des interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="03186-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="03186-116">[IMailUser : IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), ou [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="03186-116">[IMailUser : IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="03186-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="03186-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="03186-118">[in] Indicateurs qui caractérisent l’objet initial non.</span><span class="sxs-lookup"><span data-stu-id="03186-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="03186-119">Doit être une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="03186-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="03186-120">DDLWRAP_FLAG_ANSI : objet Unwrapped est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="03186-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="03186-121">DDLWRAP_FLAG_UNICODE : objet Unwrapped est au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="03186-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="03186-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="03186-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="03186-123">[in] Indicateurs pour le format de caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="03186-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="03186-124">Doit être une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="03186-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="03186-125">DDLWRAP_FLAG_ANSI : objet Wrapped est exposé en tant que ANSI.</span><span class="sxs-lookup"><span data-stu-id="03186-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="03186-126">DDLWRAP_FLAG_UNICODE : objet Wrapped est exposé au format UNICODE.</span><span class="sxs-lookup"><span data-stu-id="03186-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="03186-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="03186-127">_pIID_</span></span>
  
>  <span data-ttu-id="03186-128">[in] L’identificateur de l’interface pris en charge par l’objet non ; valeur NULL s’il s’agit inconnu.</span><span class="sxs-lookup"><span data-stu-id="03186-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="03186-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="03186-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="03186-130">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="03186-130">[in] This parameter is not used.</span></span> <span data-ttu-id="03186-131">Il doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="03186-131">It must be NULL.</span></span> 
    
<span data-ttu-id="03186-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="03186-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="03186-133">[in] Définissez ce paramètre sur **true** si _pvUnwrapped_ doit être vérifiée pour son format avant le retour à la ligne ; valeur **false** si l’objet doit être entourée sans vérification.</span><span class="sxs-lookup"><span data-stu-id="03186-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="03186-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="03186-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="03186-135">[out] Pointeur vers l’objet demandé, incluse dans le format de caractères demandé.</span><span class="sxs-lookup"><span data-stu-id="03186-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="03186-136">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="03186-136">Return values</span></span>

<span data-ttu-id="03186-137">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="03186-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="03186-138">Note</span><span class="sxs-lookup"><span data-stu-id="03186-138">Remarks</span></span>

<span data-ttu-id="03186-139">Passage d’un objet encapsulé avec _fCheckWrap_ défini sur **true** entraînera un objet non.</span><span class="sxs-lookup"><span data-stu-id="03186-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="03186-140">Quel que soit ou non l’objet retourné est encapsulé, le client est chargé de libérer la référence de l’objet renvoyé.</span><span class="sxs-lookup"><span data-stu-id="03186-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="03186-141">Lorsque vous utilisez **GetProcAddress** pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez **HrCreateNewWrappedObject@28** comme nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="03186-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03186-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03186-142">See also</span></span>

- [<span data-ttu-id="03186-143">À propos de la couche de dégradation de données API</span><span class="sxs-lookup"><span data-stu-id="03186-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="03186-144">Constantes (couche de dégradation de données API)</span><span class="sxs-lookup"><span data-stu-id="03186-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

