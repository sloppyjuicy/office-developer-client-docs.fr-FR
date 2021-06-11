---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Crée un objet accessible par un client dans un format de caractère préféré.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317604"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="adbfd-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="adbfd-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="adbfd-104">Crée un objet accessible par un client dans un format de caractère préféré.</span><span class="sxs-lookup"><span data-stu-id="adbfd-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="adbfd-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="adbfd-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="adbfd-106">Exporté par :</span><span class="sxs-lookup"><span data-stu-id="adbfd-106">Exported by:</span></span>  <br/> |<span data-ttu-id="adbfd-107">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="adbfd-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="adbfd-108">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="adbfd-108">Called by:</span></span>  <br/> |<span data-ttu-id="adbfd-109">Client</span><span class="sxs-lookup"><span data-stu-id="adbfd-109">Client</span></span>  <br/> |
|<span data-ttu-id="adbfd-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="adbfd-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="adbfd-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="adbfd-111">Outlook</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="adbfd-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="adbfd-112">Parameters</span></span>

<span data-ttu-id="adbfd-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="adbfd-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="adbfd-114">[in] L’objet d’Outlook initialement déballé.</span><span class="sxs-lookup"><span data-stu-id="adbfd-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="adbfd-115">Doit implémenter l’une des interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="adbfd-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="adbfd-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)ou [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="adbfd-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="adbfd-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="adbfd-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="adbfd-118">[in] Indicateurs qui caractérisent l’objet initial non enveloppé.</span><span class="sxs-lookup"><span data-stu-id="adbfd-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="adbfd-119">Doit être une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="adbfd-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="adbfd-120">DDLWRAP_FLAG_ANSI — L’objet unwrapped est ANSI.</span><span class="sxs-lookup"><span data-stu-id="adbfd-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="adbfd-121">DDLWRAP_FLAG_UNICODE— L’objet unwrapped est UNICODE.</span><span class="sxs-lookup"><span data-stu-id="adbfd-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="adbfd-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="adbfd-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="adbfd-123">[in] Indicateurs du format de caractère préféré.</span><span class="sxs-lookup"><span data-stu-id="adbfd-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="adbfd-124">Doit être une ou plusieurs des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="adbfd-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="adbfd-125">DDLWRAP_FLAG_ANSI: l’objet Wrapped sera exposé en tant qu’ANSI.</span><span class="sxs-lookup"><span data-stu-id="adbfd-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="adbfd-126">DDLWRAP_FLAG_UNICODE: l’objet Wrapped sera exposé en tant qu’UNICODE.</span><span class="sxs-lookup"><span data-stu-id="adbfd-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="adbfd-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="adbfd-127">_pIID_</span></span>
  
>  <span data-ttu-id="adbfd-128">[in] Identificateur de l’interface pris en charge par l’objet déballé ; définissez-la sur NULL si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="adbfd-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="adbfd-129">_agiReserved_</span><span class="sxs-lookup"><span data-stu-id="adbfd-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="adbfd-130">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="adbfd-130">[in] This parameter is not used.</span></span> <span data-ttu-id="adbfd-131">Elle doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="adbfd-131">It must be NULL.</span></span> 
    
<span data-ttu-id="adbfd-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="adbfd-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="adbfd-133">[in] Définissez ce paramètre sur **true si**  _pvUnwrapped_ doit être vérifié pour son format avant l’habillage ; si **l’objet** doit être wrapped sans vérification.</span><span class="sxs-lookup"><span data-stu-id="adbfd-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="adbfd-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="adbfd-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="adbfd-135">[out] Pointeur vers l’objet demandé, wrapped dans le format de caractère demandé.</span><span class="sxs-lookup"><span data-stu-id="adbfd-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="adbfd-136">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="adbfd-136">Return values</span></span>

<span data-ttu-id="adbfd-137">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="adbfd-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="adbfd-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="adbfd-138">Remarks</span></span>

<span data-ttu-id="adbfd-139">La transmission d’un objet wrapped avec  _fCheckWrap_ définie sur **true** entraîne un objet non enveloppé.</span><span class="sxs-lookup"><span data-stu-id="adbfd-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="adbfd-140">Que l’objet renvoyé soit wrapped ou non, le client est chargé de libérer la référence sur l’objet renvoyé.</span><span class="sxs-lookup"><span data-stu-id="adbfd-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="adbfd-141">Lorsque vous **utilisez GetProcAddress** pour rechercher l’adresse de cette fonction dans msmapi32.dll, spécifiez **HrCreateNewWrappedObject@28** comme nom de procédure.</span><span class="sxs-lookup"><span data-stu-id="adbfd-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="adbfd-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adbfd-142">See also</span></span>

- [<span data-ttu-id="adbfd-143">À propos de la couche de dégradation de données API</span><span class="sxs-lookup"><span data-stu-id="adbfd-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="adbfd-144">Constantes (API de couche de dégradation des données)</span><span class="sxs-lookup"><span data-stu-id="adbfd-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

