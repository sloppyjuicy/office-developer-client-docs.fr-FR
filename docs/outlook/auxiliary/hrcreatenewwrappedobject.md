---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Crée un objet auquel un client peut accéder dans un format de caractères préféré.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317604"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="6252c-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="6252c-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="6252c-104">Crée un objet auquel un client peut accéder dans un format de caractères préféré.</span><span class="sxs-lookup"><span data-stu-id="6252c-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6252c-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="6252c-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6252c-106">Exporté par:</span><span class="sxs-lookup"><span data-stu-id="6252c-106">Exported by:</span></span>  <br/> |<span data-ttu-id="6252c-107">msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="6252c-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="6252c-108">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="6252c-108">Called by:</span></span>  <br/> |<span data-ttu-id="6252c-109">Client</span><span class="sxs-lookup"><span data-stu-id="6252c-109">Client</span></span>  <br/> |
|<span data-ttu-id="6252c-110">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="6252c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6252c-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="6252c-111">Outlook</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="6252c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6252c-112">Parameters</span></span>

<span data-ttu-id="6252c-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="6252c-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="6252c-114">dans Objet Outlook initial non encapsulé.</span><span class="sxs-lookup"><span data-stu-id="6252c-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="6252c-115">Doit implémenter l'une des interfaces suivantes:</span><span class="sxs-lookup"><span data-stu-id="6252c-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="6252c-116">[IMailUser: IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), IMSLogon [: IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx)ou [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="6252c-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="6252c-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="6252c-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="6252c-118">dans Indicateurs qui caractérisent l'objet initial non encapsulé.</span><span class="sxs-lookup"><span data-stu-id="6252c-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="6252c-119">Doit être une ou plusieurs des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="6252c-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="6252c-120">DDLWRAP_FLAG_ANSI: l'objet non encapsulé est au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="6252c-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="6252c-121">DDLWRAP_FLAG_UNICODE: l'objet non encapsulé est UNICODE.</span><span class="sxs-lookup"><span data-stu-id="6252c-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="6252c-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="6252c-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="6252c-123">dans Indicateurs pour le format de caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="6252c-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="6252c-124">Doit être une ou plusieurs des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="6252c-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="6252c-125">DDLWRAP_FLAG_ANSI: l'objet encapsulé sera exposé en tant que ANSI.</span><span class="sxs-lookup"><span data-stu-id="6252c-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="6252c-126">DDLWRAP_FLAG_UNICODE: l'objet encapsulé sera exposé en tant que UNICODE.</span><span class="sxs-lookup"><span data-stu-id="6252c-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="6252c-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="6252c-127">_pIID_</span></span>
  
>  <span data-ttu-id="6252c-128">dans Identificateur de l'interface pris en charge par l'objet déencapsulé; Définissez-la sur NULL si cette valeur est inconnue.</span><span class="sxs-lookup"><span data-stu-id="6252c-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="6252c-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="6252c-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="6252c-130">dans Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="6252c-130">[in] This parameter is not used.</span></span> <span data-ttu-id="6252c-131">Elle doit être NULL.</span><span class="sxs-lookup"><span data-stu-id="6252c-131">It must be NULL.</span></span> 
    
<span data-ttu-id="6252c-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="6252c-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="6252c-133">dans Définissez ce paramètre sur **true** si la mise en forme de _pvUnwrapped_ doit être vérifiée avant l'encapsulation; Affectez- \*\*\*\* lui la valeur false si l'objet doit être encapsulé sans vérification.</span><span class="sxs-lookup"><span data-stu-id="6252c-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="6252c-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="6252c-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="6252c-135">remarquer Pointeur vers l'objet demandé, encapsulé dans le format de caractère demandé.</span><span class="sxs-lookup"><span data-stu-id="6252c-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="6252c-136">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="6252c-136">Return values</span></span>

<span data-ttu-id="6252c-137">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="6252c-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6252c-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="6252c-138">Remarks</span></span>

<span data-ttu-id="6252c-139">Le passage d'un objet encapsulé avec _fCheckWrap_ défini sur **true** génère un objet non encapsulé.</span><span class="sxs-lookup"><span data-stu-id="6252c-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="6252c-140">Que l'objet renvoyé soit ou non encapsulé, le client est responsable de la publication de la référence sur l'objet renvoyé.</span><span class="sxs-lookup"><span data-stu-id="6252c-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="6252c-141">Lors de l'utilisation de **GetProcAddress** pour Rechercher l'adresse de cette fonction dans msmapi32. dll, spécifiez **HrCreateNewWrappedObject @ 28** comme nom de procédure.</span><span class="sxs-lookup"><span data-stu-id="6252c-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6252c-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6252c-142">See also</span></span>

- [<span data-ttu-id="6252c-143">À propos de la couche de dégradation de données API</span><span class="sxs-lookup"><span data-stu-id="6252c-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="6252c-144">Constantes (API de la couche de dégradation des données)</span><span class="sxs-lookup"><span data-stu-id="6252c-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

