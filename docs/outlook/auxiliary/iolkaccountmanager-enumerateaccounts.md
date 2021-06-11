---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: Obtient un énumérateur pour les comptes de la catégorie spécifique ou un type.
ms.openlocfilehash: d0d383dee0e76dd6310d01bd1482e307c2374856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423047"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a><span data-ttu-id="7e074-103">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="7e074-103">IOlkAccountManager::EnumerateAccounts</span></span>

<span data-ttu-id="7e074-104">Obtient un énumérateur pour les comptes de la catégorie spécifique ou un type.</span><span class="sxs-lookup"><span data-stu-id="7e074-104">Gets an enumerator for the accounts of the specific category or type.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7e074-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7e074-105">Quick info</span></span>

<span data-ttu-id="7e074-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="7e074-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a><span data-ttu-id="7e074-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="7e074-107">Parameters</span></span>

<span data-ttu-id="7e074-108">_pclsidCategory_</span><span class="sxs-lookup"><span data-stu-id="7e074-108">_pclsidCategory_</span></span>
  
> <span data-ttu-id="7e074-p101">[in] L'identificateur de classe de la catégorie à énumérer. La valeur doit être une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7e074-p101">[in] The class identifier of the category to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="7e074-111">CLSID_OlkMail</span><span class="sxs-lookup"><span data-stu-id="7e074-111">CLSID_OlkMail</span></span> 
    
   -  <span data-ttu-id="7e074-112">CLSID_OlkAddressBook</span><span class="sxs-lookup"><span data-stu-id="7e074-112">CLSID_OlkAddressBook</span></span> 
    
   - <span data-ttu-id="7e074-113">CLSID_OlkStore</span><span class="sxs-lookup"><span data-stu-id="7e074-113">CLSID_OlkStore</span></span> 
    
<span data-ttu-id="7e074-114">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="7e074-114">_pclsidType_</span></span>
  
> <span data-ttu-id="7e074-p102">[in] L'identificateur de classe du type de compte pour énumérer. La valeur doit être une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7e074-p102">[in] The class identifier of the account type to enumerate. The value must be one of the following:</span></span>
    
   - <span data-ttu-id="7e074-117">CLSID_OlkPOP3Account</span><span class="sxs-lookup"><span data-stu-id="7e074-117">CLSID_OlkPOP3Account</span></span>
    
   - <span data-ttu-id="7e074-118">CLSID_OlkIMAP4Account</span><span class="sxs-lookup"><span data-stu-id="7e074-118">CLSID_OlkIMAP4Account</span></span>
    
   - <span data-ttu-id="7e074-119">CLSID_OlkMAPIAccount</span><span class="sxs-lookup"><span data-stu-id="7e074-119">CLSID_OlkMAPIAccount</span></span>
    
   - <span data-ttu-id="7e074-120">CLSID_OlkHotmailAccount</span><span class="sxs-lookup"><span data-stu-id="7e074-120">CLSID_OlkHotmailAccount</span></span>
    
   - <span data-ttu-id="7e074-121">CLSID_OlkLDAPAccount</span><span class="sxs-lookup"><span data-stu-id="7e074-121">CLSID_OlkLDAPAccount</span></span>
    
<span data-ttu-id="7e074-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="7e074-122">_dwFlags_</span></span>
  
> <span data-ttu-id="7e074-p103">[in] Indicateurs pour modifier le comportement. La seule valeur prise en charge est OLK_ACCOUNT_NO_FLAGS.</span><span class="sxs-lookup"><span data-stu-id="7e074-p103">[in] Flags to modify behavior. The only supported value is OLK_ACCOUNT_NO_FLAGS.</span></span>
    
<span data-ttu-id="7e074-125">_ppEnum_</span><span class="sxs-lookup"><span data-stu-id="7e074-125">_ppEnum_</span></span>
  
> <span data-ttu-id="7e074-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span><span class="sxs-lookup"><span data-stu-id="7e074-126">[out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7e074-127">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7e074-127">Return values</span></span>

|<span data-ttu-id="7e074-128">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="7e074-128">**HRESULT**</span></span>|<span data-ttu-id="7e074-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e074-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7e074-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e074-130">S_OK</span></span>  <br/> |<span data-ttu-id="7e074-131">L'appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="7e074-131">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="7e074-132">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="7e074-132">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="7e074-133">Le Gestionnaire de comptes n'a pas été initialisé pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="7e074-133">The account manager has not been initialized for use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e074-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="7e074-134">Remarks</span></span>

<span data-ttu-id="7e074-p104">Spécification de valeur NULL pour la catégorie renvoie un énumérateur de tous les comptes du type spécifié. De même, la spécification NULL pour le type renvoie un énumérateur de tous les comptes de la catégorie spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7e074-p104">Specifying NULL for category returns an enumerator of all accounts of the specified type. Similarly, specifying NULL for type returns an enumerator of all accounts of the specified category.</span></span>
  
 <span data-ttu-id="7e074-137">**IOlkAccountManager::EnumerateAccounts** ne prend pas en charge la catégorie de carnet d'adresses pour un compte Exchange.</span><span class="sxs-lookup"><span data-stu-id="7e074-137">**IOlkAccountManager::EnumerateAccounts** does not support the address book category for an Exchange account.</span></span> <span data-ttu-id="7e074-138">Si le compte est un compte Exchange (*pclsidType* est **CLSID_OlkMAPIAccount** ), et que vous essayez d’éumer les comptes qui implémentent le carnet d’adresses (*prgclsidCategory* est **CLSID_OlkAddressBook** ), l’appel de **IOlkAccountManager::EnumerateAccounts** ne retournera pas le compte Exchange dans l’éumérateur de comptes *ppEnum* .</span><span class="sxs-lookup"><span data-stu-id="7e074-138">If the account is an Exchange account (*pclsidType*  is **CLSID_OlkMAPIAccount** ), and you are trying to enumerate accounts that implement the address book (*prgclsidCategory*  is **CLSID_OlkAddressBook** ), calling **IOlkAccountManager::EnumerateAccounts** will not return the Exchange account in the accounts enumerator  *ppEnum*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e074-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e074-139">See also</span></span>

- [<span data-ttu-id="7e074-140">Constantes (API de gestion des comptes)</span><span class="sxs-lookup"><span data-stu-id="7e074-140">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="7e074-141">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="7e074-141">IOlkEnum</span></span>](iolkenum.md)

