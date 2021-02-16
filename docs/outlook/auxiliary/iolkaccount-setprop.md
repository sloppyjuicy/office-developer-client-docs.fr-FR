---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Définit la valeur de la propriété de compte spécifiée.
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431987"
---
# <a name="iolkaccountsetprop"></a><span data-ttu-id="a3b34-103">IOlkAccount::SetProp</span><span class="sxs-lookup"><span data-stu-id="a3b34-103">IOlkAccount::SetProp</span></span>

<span data-ttu-id="a3b34-104">Définit la valeur de la propriété de compte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a3b34-104">Sets the value of the specified account property.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a3b34-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a3b34-105">Quick info</span></span>

<span data-ttu-id="a3b34-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a3b34-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a><span data-ttu-id="a3b34-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3b34-107">Parameters</span></span>

<span data-ttu-id="a3b34-108">_dwProp_</span><span class="sxs-lookup"><span data-stu-id="a3b34-108">_dwProp_</span></span>
  
> <span data-ttu-id="a3b34-109">[in] Balise de propriété de la propriété de compte à définir.</span><span class="sxs-lookup"><span data-stu-id="a3b34-109">[in] The property tag of the account property to set.</span></span>
    
<span data-ttu-id="a3b34-110">_pVar_</span><span class="sxs-lookup"><span data-stu-id="a3b34-110">_pVar_</span></span>
  
> <span data-ttu-id="a3b34-111">[in] Valeur de la propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a3b34-111">[in] The value of the specified property.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="a3b34-112">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="a3b34-112">Return values</span></span>

|<span data-ttu-id="a3b34-113">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="a3b34-113">**HRESULT**</span></span>|<span data-ttu-id="a3b34-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="a3b34-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3b34-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3b34-115">S_OK</span></span>  <br/> |<span data-ttu-id="a3b34-116">L’appel de méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a3b34-116">The method call was successful.</span></span>  <br/> |
|<span data-ttu-id="a3b34-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a3b34-117">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="a3b34-118">Une balise de propriété non valide a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a3b34-118">An invalid property tag was specified.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3b34-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3b34-119">Remarks</span></span>

<span data-ttu-id="a3b34-120">Utilisez [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) pour enregistrer les modifications apportées à la valeur des propriétés du compte.</span><span class="sxs-lookup"><span data-stu-id="a3b34-120">Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) to save changes to the value of account properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a3b34-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3b34-121">See also</span></span>

- [<span data-ttu-id="a3b34-122">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="a3b34-122">Constants (Account management API)</span></span>](constants-account-management-api.md) 
- [<span data-ttu-id="a3b34-123">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="a3b34-123">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

