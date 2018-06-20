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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dcde242f5f2e956d1926d6914431008383f5aa55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783932"
---
# <a name="imapisessionopenaddressbook"></a><span data-ttu-id="45f89-103">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="45f89-103">IMAPISession::OpenAddressBook</span></span>

  
  
<span data-ttu-id="45f89-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45f89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45f89-105">Ouvre le carnet d’adresses intégré MAPI, qui retourne un pointeur [IAddrBook](iaddrbookimapiprop.md) pour davantage d’accès.</span><span class="sxs-lookup"><span data-stu-id="45f89-105">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenAddressBook(
  ULONG_PTR ulUIParam,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPADRBOOK FAR * lppAdrBook
);
```

## <a name="parameters"></a><span data-ttu-id="45f89-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45f89-106">Parameters</span></span>

 <span data-ttu-id="45f89-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="45f89-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="45f89-108">[in] Un handle vers la fenêtre parent de la boîte de dialogue commune adresse et d’autres liées affiche.</span><span class="sxs-lookup"><span data-stu-id="45f89-108">[in] A handle to the parent window of the common address dialog box and other related displays.</span></span>
    
 <span data-ttu-id="45f89-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="45f89-109">_lpInterface_</span></span>
  
> <span data-ttu-id="45f89-110">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="45f89-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the address book.</span></span> <span data-ttu-id="45f89-111">Interface standard du carnet d’adresses, en passant **null** renvoie un pointeur [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="45f89-111">Passing **null** returns a pointer to the address book's standard interface, [IAddrBook : IMAPIProp](iaddrbookimapiprop.md).</span></span> 
    
 <span data-ttu-id="45f89-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="45f89-112">_ulFlags_</span></span>
  
> <span data-ttu-id="45f89-113">[in] Masque de bits d’indicateurs qui contrôle l’ouverture du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="45f89-113">[in] A bitmask of flags that controls the opening of the address book.</span></span> <span data-ttu-id="45f89-114">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="45f89-114">The following flag can be set:</span></span>
    
<span data-ttu-id="45f89-115">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="45f89-115">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="45f89-116">Supprime l’affichage des boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="45f89-116">Suppresses the display of dialog boxes.</span></span> <span data-ttu-id="45f89-117">Si l’indicateur AB_NO_DIALOG n’est pas définie, les fournisseurs de carnet d’adresses qui contribuent au carnet d’adresses intégré peuvent inviter l’utilisateur à toutes les informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="45f89-117">If the AB_NO_DIALOG flag is not set, the address book providers that contribute to the integrated address book can prompt the user for any necessary information.</span></span> 
    
 <span data-ttu-id="45f89-118">_lppAdrBook_</span><span class="sxs-lookup"><span data-stu-id="45f89-118">_lppAdrBook_</span></span>
  
> <span data-ttu-id="45f89-119">[out] Pointeur vers un pointeur vers le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="45f89-119">[out] A pointer to a pointer to the address book.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="45f89-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="45f89-120">Return value</span></span>

<span data-ttu-id="45f89-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="45f89-121">S_OK</span></span> 
  
> <span data-ttu-id="45f89-122">Le carnet d’adresses a été ouvert avec succès.</span><span class="sxs-lookup"><span data-stu-id="45f89-122">The address book was successfully opened.</span></span>
    
<span data-ttu-id="45f89-123">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="45f89-123">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="45f89-124">L’appel a réussi, mais les conteneurs d’un ou plusieurs fournisseurs de carnet d’adresses n’a pas peuvent être ouvert.</span><span class="sxs-lookup"><span data-stu-id="45f89-124">The call succeeded, but the containers of one or more address book providers could not be opened.</span></span> <span data-ttu-id="45f89-125">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi.</span><span class="sxs-lookup"><span data-stu-id="45f89-125">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="45f89-126">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="45f89-126">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="45f89-127">Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="45f89-127">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45f89-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="45f89-128">Remarks</span></span>

<span data-ttu-id="45f89-129">La méthode **IMAPISession::OpenAddressBook** ouvre le carnet d’adresses intégré MAPI, une collection des conteneurs de tous les fournisseurs de carnet d’adresses dans le profil de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="45f89-129">The **IMAPISession::OpenAddressBook** method opens the MAPI integrated address book, a collection of the top-level containers of all of the address book providers in the profile.</span></span> <span data-ttu-id="45f89-130">Le pointeur est retourné dans le paramètre _lppAdrBook_ fournit davantage l’accès au contenu du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="45f89-130">The pointer that is returned in the  _lppAdrBook_ parameter provides further access to the contents of the address book.</span></span> <span data-ttu-id="45f89-131">Cela permet à l’appelant effectuer des tâches telles que l’ouverture des conteneurs individuels, recherche des utilisateurs de messagerie et l’affichage des boîtes de dialogue communes adresse.</span><span class="sxs-lookup"><span data-stu-id="45f89-131">This allows the caller to perform tasks such as opening individual containers, finding messaging users, and displaying common address dialog boxes.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="45f89-132">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="45f89-132">Notes to callers</span></span>

 <span data-ttu-id="45f89-133">**OpenAddressBook** renvoie MAPI_W_ERRORS_RETURNED si elle ne peut pas charger une ou plusieurs des fournisseurs de carnet d’adresses dans le profil.</span><span class="sxs-lookup"><span data-stu-id="45f89-133">**OpenAddressBook** returns MAPI_W_ERRORS_RETURNED if it cannot load one or more of the address book providers in the profile.</span></span> <span data-ttu-id="45f89-134">Cette valeur est un message d’avertissement, pas une valeur d’erreur ; gérer comme vous le feriez S_OK.</span><span class="sxs-lookup"><span data-stu-id="45f89-134">This value is a warning, not an error value; handle it as you would S_OK.</span></span> <span data-ttu-id="45f89-135">**OpenAddressBook** renvoie toujours un pointeur valide dans le paramètre _lppAdrBook_ , quel que soit le nombre des fournisseurs de carnet d’adresses n’a pas pu charger.</span><span class="sxs-lookup"><span data-stu-id="45f89-135">**OpenAddressBook** always returns a valid pointer in the  _lppAdrBook_ parameter, regardless of how many of the address book providers failed to load.</span></span> <span data-ttu-id="45f89-136">Par conséquent, vous devez toujours appeler méthode de [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) du carnet d’adresses à un moment donné avant la fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="45f89-136">Therefore, you must always call the address book's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method at some point before logging off.</span></span> 
  
<span data-ttu-id="45f89-137">Lorsque **OpenAddressBook** renvoie MAPI_W_ERRORS_RETURNED, appelez [IMAPISession::GetLastError](imapisession-getlasterror.md) pour obtenir une structure [MAPIERROR](mapierror.md) qui contient des informations sur les fournisseurs défectueux.</span><span class="sxs-lookup"><span data-stu-id="45f89-137">When **OpenAddressBook** returns MAPI_W_ERRORS_RETURNED, call [IMAPISession::GetLastError](imapisession-getlasterror.md) to obtain a [MAPIERROR](mapierror.md) structure that contains information about the failing providers.</span></span> <span data-ttu-id="45f89-138">Une structure **MAPIERROR** unique est retournée qui contient les informations fournies par tous les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="45f89-138">A single **MAPIERROR** structure is returned that contains information supplied by all of the providers.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="45f89-139">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="45f89-139">MFCMAPI reference</span></span>

<span data-ttu-id="45f89-140">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="45f89-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="45f89-141">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="45f89-141">**File**</span></span>|<span data-ttu-id="45f89-142">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="45f89-142">**Function**</span></span>|<span data-ttu-id="45f89-143">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="45f89-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45f89-144">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="45f89-144">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="45f89-145">CMapiObjects::GetAddrBook</span><span class="sxs-lookup"><span data-stu-id="45f89-145">CMapiObjects::GetAddrBook</span></span>  <br/> |<span data-ttu-id="45f89-146">MFCMAPI utilise la méthode **IMAPISession::OpenAddressBook** pour obtenir le carnet d’adresses intégré.</span><span class="sxs-lookup"><span data-stu-id="45f89-146">MFCMAPI uses the **IMAPISession::OpenAddressBook** method to obtain the integrated address book.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45f89-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45f89-147">See also</span></span>



[<span data-ttu-id="45f89-148">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="45f89-148">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="45f89-149">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="45f89-149">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="45f89-150">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="45f89-150">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="45f89-151">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45f89-151">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="45f89-152">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="45f89-152">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

