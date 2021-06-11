---
title: IMAPISessionOpenAddressBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenAddressBook
api_type:
- COM
ms.assetid: 2b6a4c6a-bb71-4ea1-a3b6-90a2722880fb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 51bf5f8455d4cb790d0c955e96249b0f9deef1af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329420"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="6fef1-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="6fef1-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="6fef1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fef1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fef1-105">Ouvre le carnet d’adresses intégré MAPI, en renvoyant un [pointeur IAddrBook](iaddrbookimapiprop.md) pour un accès supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="6fef1-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="6fef1-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6fef1-106">Parameters</span></span>

 <span data-ttu-id="6fef1-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6fef1-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="6fef1-108">[in] Poignée vers la fenêtre parente de la boîte de dialogue d’adresse commune et autres affichages associés.</span><span class="sxs-lookup"><span data-stu-id="6fef1-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="6fef1-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6fef1-109">_lpInterface_</span></span>
  
> <span data-ttu-id="6fef1-110">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6fef1-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="6fef1-111">La **transmission de la** valeur null renvoie un pointeur vers l’interface standard du carnet d’adresses, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="6fef1-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="6fef1-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6fef1-112">_ulFlags_</span></span>
  
> <span data-ttu-id="6fef1-113">[in] Masque de bits d’indicateurs qui contrôle l’ouverture du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6fef1-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="6fef1-114">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="6fef1-114">The following flag can be set:</span></span>
    
<span data-ttu-id="6fef1-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6fef1-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="6fef1-116">Supprime l’affichage des boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6fef1-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="6fef1-117">Si l’AB_NO_DIALOG n’est pas définie, les fournisseurs de carnet d’adresses qui contribuent au carnet d’adresses intégré peuvent inviter l’utilisateur à fournir les informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="6fef1-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="6fef1-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="6fef1-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="6fef1-119">[out] Pointeur vers un pointeur vers le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6fef1-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fef1-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6fef1-120">Return value</span></span>

<span data-ttu-id="6fef1-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fef1-121">S_OK</span></span> 
  
> <span data-ttu-id="6fef1-122">Le carnet d’adresses a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="6fef1-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="6fef1-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="6fef1-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="6fef1-124">L’appel a réussi, mais les conteneurs d’un ou plusieurs fournisseurs de carnet d’adresses n’ont pas pu être ouverts.</span><span class="sxs-lookup"><span data-stu-id="6fef1-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="6fef1-125">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi.</span><span class="sxs-lookup"><span data-stu-id="6fef1-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="6fef1-126">Pour tester cet avertissement, utilisez la macro **HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="6fef1-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="6fef1-127">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="6fef1-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fef1-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="6fef1-128">Remarks</span></span>

<span data-ttu-id="6fef1-129">La **méthode IMAPISession::OpenAddressBook** ouvre le carnet d’adresses intégré MAPI, une collection des conteneurs de niveau supérieur de tous les fournisseurs de carnet d’adresses du profil.</span><span class="sxs-lookup"><span data-stu-id="6fef1-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="6fef1-130">Le pointeur renvoyé dans le  _paramètre lppAdrBook_ fournit un accès supplémentaire au contenu du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6fef1-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="6fef1-131">Cela permet à l’appelant d’effectuer des tâches telles que l’ouverture de conteneurs individuels, la recherche d’utilisateurs de messagerie et l’affichage de boîtes de dialogue d’adresse communes.</span><span class="sxs-lookup"><span data-stu-id="6fef1-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6fef1-132">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="6fef1-132">Notes to callers</span></span>

 <span data-ttu-id="6fef1-133">**OpenAddressBook renvoie** MAPI_W_ERRORS_RETURNED si elle ne peut pas charger un ou plusieurs des fournisseurs de carnet d’adresses dans le profil.</span><span class="sxs-lookup"><span data-stu-id="6fef1-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="6fef1-134">Cette valeur est un avertissement, et non une valeur d’erreur . gérer comme vous le feriez S_OK.</span><span class="sxs-lookup"><span data-stu-id="6fef1-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="6fef1-135">**OpenAddressBook renvoie** toujours un pointeur valide dans le paramètre  _lppAdrBook,_ quel que soit le nombre de fournisseurs de carnet d’adresses dont le chargement a échoué.</span><span class="sxs-lookup"><span data-stu-id="6fef1-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="6fef1-136">Par conséquent, vous devez toujours appeler la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) du carnet d’adresses à un moment donné avant de vous dé connecter.</span><span class="sxs-lookup"><span data-stu-id="6fef1-136">Therefore, you must always call the address book's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="6fef1-137">Lorsque **OpenAddressBook** renvoie MAPI_W_ERRORS_RETURNED, appelez [IMAPISession::GetLastError](imapisession-getlasterror.md) pour obtenir une structure [MAPIERROR](mapierror.md) qui contient des informations sur les fournisseurs défaillants.</span><span class="sxs-lookup"><span data-stu-id="6fef1-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="6fef1-138">Une structure **MAPIERROR unique** qui contient les informations fournies par tous les fournisseurs est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="6fef1-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6fef1-139">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6fef1-139">MFCMAPI reference</span></span>

<span data-ttu-id="6fef1-140">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6fef1-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6fef1-141">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6fef1-141">**File**</span></span>|<span data-ttu-id="6fef1-142">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6fef1-142">**Function**</span></span>|<span data-ttu-id="6fef1-143">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6fef1-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6fef1-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="6fef1-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="6fef1-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="6fef1-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="6fef1-146">MFCMAPI utilise la **méthode IMAPISession::OpenAddressBook** pour obtenir le carnet d’adresses intégré.</span><span class="sxs-lookup"><span data-stu-id="6fef1-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fef1-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fef1-147">See also</span></span>



[<span data-ttu-id="6fef1-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6fef1-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="6fef1-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6fef1-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="6fef1-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6fef1-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6fef1-151">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6fef1-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="6fef1-152">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6fef1-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

