---
title: IMAPISupportOpenAddressBook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenAddressBook
api_type:
- COM
ms.assetid: d8da8be1-3efe-410a-bcce-49e522602d80
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 26550691ef959fa7cefa83827dd1391538bd2d38
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588173"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="3ca05-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="3ca05-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="3ca05-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ca05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ca05-105">Fournit l’accès au carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3ca05-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="3ca05-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ca05-106">Parameters</span></span>

 <span data-ttu-id="3ca05-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="3ca05-107">_lpInterface_</span></span>
  
> <span data-ttu-id="3ca05-108">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3ca05-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="3ca05-109">Les valeurs valides sont NULL, ce qui indique l’interface de carnet d’adresses standard [IAddrBook](iaddrbookimapiprop.md)et IID_IAddrBook.</span><span class="sxs-lookup"><span data-stu-id="3ca05-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="3ca05-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ca05-110">_ulFlags_</span></span>
  
> <span data-ttu-id="3ca05-111">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3ca05-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3ca05-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="3ca05-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="3ca05-113">[out] Pointeur vers un pointeur vers le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3ca05-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ca05-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3ca05-114">Return value</span></span>

<span data-ttu-id="3ca05-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ca05-115">S_OK</span></span> 
  
> <span data-ttu-id="3ca05-116">Accès au carnet d’adresses a été fournie.</span><span class="sxs-lookup"><span data-stu-id="3ca05-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="3ca05-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="3ca05-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="3ca05-118">L’appel a réussi, mais un ou plusieurs fournisseurs de carnet d’adresses n’a pas peuvent être chargés.</span><span class="sxs-lookup"><span data-stu-id="3ca05-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="3ca05-119">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="3ca05-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="3ca05-120">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="3ca05-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="3ca05-121">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="3ca05-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ca05-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="3ca05-122">Remarks</span></span>

<span data-ttu-id="3ca05-123">La méthode **IMAPISupport::OpenAddressBook** est implémentée pour tous les objets de prise en charge de fournisseur de service.</span><span class="sxs-lookup"><span data-stu-id="3ca05-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="3ca05-124">Fournisseurs de services, généralement étroitement couplé message stockent et fournisseurs de transport, appelez **OpenAddressBook** pour obtenir l’accès au carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="3ca05-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="3ca05-125">Le pointeur de **IAddrBook** retourné peut être utilisé pour diverses tâches de carnet d’adresses, y compris l’ouverture des conteneurs de carnet d’adresses, recherche des utilisateurs de messagerie et de boîtes de dialogue affichage adresse.</span><span class="sxs-lookup"><span data-stu-id="3ca05-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3ca05-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="3ca05-126">Notes to callers</span></span>

 <span data-ttu-id="3ca05-127">**OpenAddressBook** peut renvoyer MAPI_W_ERRORS_RETURNED si elle ne peut pas charger une ou plusieurs des fournisseurs de carnet d’adresses dans le profil actif.</span><span class="sxs-lookup"><span data-stu-id="3ca05-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="3ca05-128">Cette valeur est un avertissement et vous devez traiter l’appel comme réussie.</span><span class="sxs-lookup"><span data-stu-id="3ca05-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="3ca05-129">Même si tous les fournisseurs de carnet d’adresses Échec du chargement, **OpenAddressBook** toujours réussit, renvoyant MAPI_W_ERRORS_RETURNED et un pointeur **IAddrBook** dans le paramètre _lppAdrBook_ .</span><span class="sxs-lookup"><span data-stu-id="3ca05-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="3ca05-130">Étant donné que **OpenAddressBook** retourne toujours un pointeur **IAddrBook** valide, vous devez le libérer lorsque vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="3ca05-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="3ca05-131">Impossible de charger un ou plusieurs fournisseurs de carnet d’adresses, appelez [IMAPISupport::GetLastError](imapisupport-getlasterror.md) pour obtenir une structure [MAPIERROR](mapierror.md) qui contient des informations sur les fournisseurs qui n’a pas été chargé.</span><span class="sxs-lookup"><span data-stu-id="3ca05-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ca05-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ca05-132">See also</span></span>



[<span data-ttu-id="3ca05-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3ca05-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="3ca05-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="3ca05-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="3ca05-135">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ca05-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

