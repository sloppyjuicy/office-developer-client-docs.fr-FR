---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: Obtient les informations de type et de catégorie pour le compte spécifié.
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437902"
---
# <a name="iolkaccountgetaccountinfo"></a><span data-ttu-id="8885d-103">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="8885d-103">IOlkAccount::GetAccountInfo</span></span>

<span data-ttu-id="8885d-104">Obtient les informations de type et de catégorie pour le compte spécifié.</span><span class="sxs-lookup"><span data-stu-id="8885d-104">Gets the type and categories information for the specified account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8885d-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="8885d-105">Quick info</span></span>

<span data-ttu-id="8885d-106">Voir [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="8885d-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a><span data-ttu-id="8885d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8885d-107">Parameters</span></span>

<span data-ttu-id="8885d-108">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="8885d-108">_pclsidType_</span></span>
  
> <span data-ttu-id="8885d-109">remarquer Identificateur de classe du type de compte.</span><span class="sxs-lookup"><span data-stu-id="8885d-109">[out] The class identifier for the account type.</span></span> <span data-ttu-id="8885d-110">La valeur doit être une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="8885d-110">The value must be one of the following:</span></span>
    
   - <span data-ttu-id="8885d-111">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="8885d-111">CLSID_OlkPOP3Account</span></span> 
    
   - <span data-ttu-id="8885d-112">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="8885d-112">CLSID_OlkIMAP4Account</span></span> 
    
   - <span data-ttu-id="8885d-113">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="8885d-113">CLSID_OlkMAPIAccount</span></span> 
    
   - <span data-ttu-id="8885d-114">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="8885d-114">CLSID_OlkHotmailAccount</span></span> 
    
   - <span data-ttu-id="8885d-115">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="8885d-115">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="8885d-116">_pcCategories_</span><span class="sxs-lookup"><span data-stu-id="8885d-116">_pcCategories_</span></span>
  
> <span data-ttu-id="8885d-117">remarquer Nombre de catégories dans _prgclsidCategory_.</span><span class="sxs-lookup"><span data-stu-id="8885d-117">[out] The number of categories in  _prgclsidCategory_.</span></span>
    
<span data-ttu-id="8885d-118">_prgclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="8885d-118">_prgclsidCategory_</span></span>
  
> <span data-ttu-id="8885d-119">remarquer Tableau de catégories auquel ce compte est associé.</span><span class="sxs-lookup"><span data-stu-id="8885d-119">[out] An array of categories that this account is associated with.</span></span> <span data-ttu-id="8885d-120">Le tableau est de taille \* _pcCategories_.</span><span class="sxs-lookup"><span data-stu-id="8885d-120">The array is of size \* _pcCategories_.</span></span> <span data-ttu-id="8885d-121">La valeur de chaque catégorie dans le tableau doit être l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="8885d-121">The value of each category in the array must be one of the following:</span></span>
    
   - <span data-ttu-id="8885d-122">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="8885d-122">CLSID_OlkMail</span></span>
    
   - <span data-ttu-id="8885d-123">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="8885d-123">CLSID_OlkAddressBook</span></span>
    
   - <span data-ttu-id="8885d-124">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="8885d-124">CLSID_OlkStore</span></span>
    
## <a name="return-values"></a><span data-ttu-id="8885d-125">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="8885d-125">Return values</span></span>

<span data-ttu-id="8885d-126">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="8885d-126">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8885d-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="8885d-127">Remarks</span></span>

<span data-ttu-id="8885d-128">Une fois cette méthode retournée, vous devez libérer *prgclsidCategory* à l'aide de [IOlkAccount:: FreeMemory](iolkaccount-freememory.md).</span><span class="sxs-lookup"><span data-stu-id="8885d-128">After this method returns, you must free  *prgclsidCategory*  by using [IOlkAccount::FreeMemory](iolkaccount-freememory.md).</span></span>
  
<span data-ttu-id="8885d-129">**IOlkAccount:: GetAccountInfo** ne prend pas en charge la catégorie de carnet d'adresses pour un compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="8885d-129">**IOlkAccount::GetAccountInfo** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="8885d-130">Si le compte est un compte Exchange (*pclsidType* est **CLSID_OlkMAPIAccount** ) et que le compte implémente le carnet d'adresses, l'appel de **IOlkAccount:: GetAccountInfo** ne renverra pas **CLSID_OlkAddressBook** sous forme de catégorie dans \* prgclsidCategory\* .</span><span class="sxs-lookup"><span data-stu-id="8885d-130">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and the account implements the address book, calling **IOlkAccount::GetAccountInfo** will not return **CLSID_OlkAddressBook** as a category in  *prgclsidCategory*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8885d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8885d-131">See also</span></span>

- [<span data-ttu-id="8885d-132">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="8885d-132">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="8885d-133">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="8885d-133">IOlkAccount::FreeMemory</span></span>](iolkaccount-freememory.md)

