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
ms.openlocfilehash: 47a62b331ff9f1c96576d42797ebb23ed61cd362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416880"
---
# <a name="imapisupportopenaddressbook"></a><span data-ttu-id="dcfd0-103">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="dcfd0-103">IMAPISupport::OpenAddressBook</span></span>

  
  
<span data-ttu-id="dcfd0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcfd0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcfd0-105">Permet d’accéder au carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-105">Provides access to the address book.</span></span>
  
```cpp
HRESULT OpenAddressBook(
LPCIID lpInterface,
ULONG ulFlags,
LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="dcfd0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcfd0-106">Parameters</span></span>

 <span data-ttu-id="dcfd0-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="dcfd0-107">_lpInterface_</span></span>
  
> <span data-ttu-id="dcfd0-108">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="dcfd0-109">Les valeurs valides sont NULL, ce qui indique l’interface de carnet d’adresses standard [IAddrBook](iaddrbookimapiprop.md)et IID_IAddrBook.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-109">Valid values are NULL, which indicates the standard address book interface [IAddrBook](iaddrbookimapiprop.md), and IID_IAddrBook.</span></span>
    
 <span data-ttu-id="dcfd0-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dcfd0-110">_ulFlags_</span></span>
  
> <span data-ttu-id="dcfd0-111">Réservé ; doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-111">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="dcfd0-112">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="dcfd0-112">_lppAdrBook_</span></span>
  
> <span data-ttu-id="dcfd0-113">[out] Pointeur vers un pointeur vers le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-113">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dcfd0-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dcfd0-114">Return value</span></span>

<span data-ttu-id="dcfd0-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="dcfd0-115">S_OK</span></span> 
  
> <span data-ttu-id="dcfd0-116">L’accès au carnet d’adresses a été fourni.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-116">Access to the address book was provided.</span></span>
    
<span data-ttu-id="dcfd0-117">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="dcfd0-117">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="dcfd0-118">L’appel a réussi, mais un ou plusieurs fournisseurs de carnet d’adresses n’ont pas pu être chargés.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-118">The call succeeded, but one or more address book providers could not be loaded.</span></span> <span data-ttu-id="dcfd0-119">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-119">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="dcfd0-120">Pour tester cet avertissement, utilisez la macro **HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="dcfd0-120">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="dcfd0-121">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="dcfd0-121">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dcfd0-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="dcfd0-122">Remarks</span></span>

<span data-ttu-id="dcfd0-123">La **méthode IMAPISupport::OpenAddressBook** est implémentée pour tous les objets de prise en charge du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-123">The **IMAPISupport::OpenAddressBook** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="dcfd0-124">Les fournisseurs de services, généralement étroitement associés aux fournisseurs de transport et de magasin de messages, appellent **OpenAddressBook** pour accéder au carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-124">Service providers, typically tightly coupled message store and transport providers, call **OpenAddressBook** to get access to the address book.</span></span> <span data-ttu-id="dcfd0-125">Le pointeur **IAddrBook** renvoyé peut être utilisé pour diverses tâches de carnet d’adresses, notamment l’ouverture de conteneurs de carnet d’adresses, la recherche d’utilisateurs de messagerie et l’affichage de boîtes de dialogue d’adresses.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-125">The returned **IAddrBook** pointer can be used for a variety of address book tasks, including opening address book containers, finding messaging users, and displaying address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dcfd0-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="dcfd0-126">Notes to callers</span></span>

 <span data-ttu-id="dcfd0-127">**OpenAddressBook peut** renvoyer MAPI_W_ERRORS_RETURNED s’il ne peut pas charger un ou plusieurs des fournisseurs de carnet d’adresses dans le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-127">**OpenAddressBook** can return MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the current profile.</span></span> <span data-ttu-id="dcfd0-128">Cette valeur est un avertissement et vous devez traiter l’appel comme réussi.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-128">This value is a warning and you should treat the call as successful.</span></span> <span data-ttu-id="dcfd0-129">Même si tous les fournisseurs de carnet d’adresses n’ont pas réussi à se charger, **OpenAddressBook** réussit toujours, renvoyant MAPI_W_ERRORS_RETURNED et un pointeur **IAddrBook** dans le paramètre _lppAdrBook._</span><span class="sxs-lookup"><span data-stu-id="dcfd0-129">Even if all of the address book providers failed to load, **OpenAddressBook** still succeeds, returning MAPI_W_ERRORS_RETURNED and an **IAddrBook** pointer in the  _lppAdrBook_ parameter.</span></span> <span data-ttu-id="dcfd0-130">Étant **donné qu’OpenAddressBook** renvoie toujours un pointeur **IAddrBook** valide, vous devez le libérer lorsque vous avez terminé de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-130">Because **OpenAddressBook** always returns a valid **IAddrBook** pointer, you must release it when you are finished using it.</span></span> 
  
<span data-ttu-id="dcfd0-131">Si un ou plusieurs fournisseurs de carnet d’adresses n’ont pas pu être chargés, appelez [IMAPISupport::GetLastError](imapisupport-getlasterror.md) pour obtenir une structure [MAPIERROR](mapierror.md) qui contient des informations sur les fournisseurs qui n’ont pas été chargés.</span><span class="sxs-lookup"><span data-stu-id="dcfd0-131">If one or more address book providers failed to load, call [IMAPISupport::GetLastError](imapisupport-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the providers that did not load.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dcfd0-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcfd0-132">See also</span></span>



[<span data-ttu-id="dcfd0-133">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dcfd0-133">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="dcfd0-134">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="dcfd0-134">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="dcfd0-135">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dcfd0-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

