---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432379"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="739fa-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="739fa-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="739fa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="739fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="739fa-105">Définit une fonction de rappel invoquée par l’Assistant Profil pour permettre à un fournisseur de services de réagir aux événements utilisateur lorsque les feuilles de propriétés ou les pages du fournisseur sont affichées.</span><span class="sxs-lookup"><span data-stu-id="739fa-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="739fa-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="739fa-106">Header file:</span></span>  <br/> |<span data-ttu-id="739fa-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="739fa-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="739fa-108">Fonction définie implémentée par :</span><span class="sxs-lookup"><span data-stu-id="739fa-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="739fa-109">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="739fa-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="739fa-110">Fonction définie appelée par :</span><span class="sxs-lookup"><span data-stu-id="739fa-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="739fa-111">Assistant Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="739fa-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="739fa-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="739fa-112">Parameters</span></span>

<span data-ttu-id="739fa-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="739fa-113">_hDlg_</span></span>
  
> <span data-ttu-id="739fa-114">[in] Poignée de fenêtre de la boîte de dialogue Assistant Profil.</span><span class="sxs-lookup"><span data-stu-id="739fa-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="739fa-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="739fa-115">_wMsgID_</span></span>
  
> <span data-ttu-id="739fa-116">[in] Message de fenêtre à traiter.</span><span class="sxs-lookup"><span data-stu-id="739fa-116">[in] The window message to be processed.</span></span> <span data-ttu-id="739fa-117">Outre les messages de fenêtre ordinaire attendus par une boîte de dialogue modale, les messages suivants peuvent être reçus :</span><span class="sxs-lookup"><span data-stu-id="739fa-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="739fa-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="739fa-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="739fa-119">L’Assistant Profil est terminé.</span><span class="sxs-lookup"><span data-stu-id="739fa-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="739fa-120">Le fournisseur de services doit faire tous les nettoyages requis, tels que la désaffectation de toute mémoire allouée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="739fa-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="739fa-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="739fa-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="739fa-122">L’un des contrôles du fournisseur a  été  sélectionné ou l’utilisateur a cliqué sur le bouton Suivant ou Arrière.</span><span class="sxs-lookup"><span data-stu-id="739fa-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="739fa-123">La valeur dans le  _paramètre wParam_ indique lequel de ces événements utilisateur s’est produit.</span><span class="sxs-lookup"><span data-stu-id="739fa-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="739fa-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="739fa-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="739fa-125">L’utilisateur a été déplacé vers une autre page de propriétés, pour laquelle la boîte de dialogue doit être initialisée.</span><span class="sxs-lookup"><span data-stu-id="739fa-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="739fa-126">Le fournisseur doit initialiser les contrôles que l’Assistant Profil a ajoutés à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="739fa-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="739fa-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="739fa-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="739fa-128">L’Assistant Profil vous invite à afficher le nombre de pages que le fournisseur doit afficher.</span><span class="sxs-lookup"><span data-stu-id="739fa-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="739fa-129">Le fournisseur doit renvoyer le nombre de pages au lieu de TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="739fa-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="739fa-130">Par exemple, utilisez l’instruction de retour suivante pour indiquer que trois pages doivent être affichées :</span><span class="sxs-lookup"><span data-stu-id="739fa-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="739fa-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="739fa-131">_wParam_</span></span>
  
> <span data-ttu-id="739fa-132">[in] Paramètre 32 bits associé aux messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="739fa-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="739fa-133">Les valeurs possibles dépendent du message spécifié dans le _paramètre wMsgID._</span><span class="sxs-lookup"><span data-stu-id="739fa-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="739fa-134">Outre les valeurs attendues avec les messages de fenêtre normal pour une boîte de dialogue modale, les valeurs suivantes peuvent être reçues :</span><span class="sxs-lookup"><span data-stu-id="739fa-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="739fa-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="739fa-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="739fa-136">Lorsque  _wMsgID_ contient WM_COMMAND, l’utilisateur a cliqué sur **le bouton** Suivant.</span><span class="sxs-lookup"><span data-stu-id="739fa-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="739fa-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="739fa-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="739fa-138">Lorsque  _wMsgID_ contient WM_COMMAND, l’utilisateur a cliqué sur le **bouton** Retour.</span><span class="sxs-lookup"><span data-stu-id="739fa-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="739fa-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="739fa-139">_lParam_</span></span>
  
> <span data-ttu-id="739fa-140">[in] Paramètre 32 bits associé aux messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="739fa-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="739fa-141">Les valeurs possibles dépendent du message spécifié dans le _paramètre wMsgID._</span><span class="sxs-lookup"><span data-stu-id="739fa-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="739fa-142">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="739fa-142">Return value</span></span>

<span data-ttu-id="739fa-143">La valeur renvoyée par une fonction basée sur **SERVICEWIZARDDLGPROC** dépend du message de fenêtre reçu.</span><span class="sxs-lookup"><span data-stu-id="739fa-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="739fa-144">Notez en particulier la valeur de retour exceptionnelle du message WIZ_QUERYNUMPAGES message.</span><span class="sxs-lookup"><span data-stu-id="739fa-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="739fa-145">Les valeurs de retour normales sont :</span><span class="sxs-lookup"><span data-stu-id="739fa-145">The normal return values are:</span></span> 
  
<span data-ttu-id="739fa-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="739fa-146">TRUE</span></span> 
  
> <span data-ttu-id="739fa-147">Le fournisseur de services a traitée le message de fenêtre reçue.</span><span class="sxs-lookup"><span data-stu-id="739fa-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="739fa-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="739fa-148">FALSE</span></span> 
  
> <span data-ttu-id="739fa-149">Le fournisseur de services n’a pas traitée le message de fenêtre reçue.</span><span class="sxs-lookup"><span data-stu-id="739fa-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="739fa-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="739fa-150">Remarks</span></span>

<span data-ttu-id="739fa-151">Lorsque l’utilisateur passe d’une page de propriétés à une autre, le fournisseur est chargé de masquer les contrôles de l’ancienne page et d’afficher les contrôles de la page suivante ou précédente.</span><span class="sxs-lookup"><span data-stu-id="739fa-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="739fa-152">Lorsque l’utilisateur  clique sur le bouton Suivant, la fonction basée sur **SERVICEWIZARDDLGPROC** est appelée avec le message WM_COMMAND et WIZ_NEXT dans le paramètre _wParam._</span><span class="sxs-lookup"><span data-stu-id="739fa-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="739fa-153">Les étapes suivantes décrivent ce qui se produit entre le moment où l’utilisateur clique sur **Next** et le moment où les pages de configuration du premier fournisseur sont restituer.</span><span class="sxs-lookup"><span data-stu-id="739fa-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="739fa-154">L’Assistant Profil masque tous les contrôles de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="739fa-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="739fa-155">L’Assistant Profil ajoute les contrôles masqués du fournisseur à la page.</span><span class="sxs-lookup"><span data-stu-id="739fa-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="739fa-156">L’Assistant Profil appelle **SERVICEWIZARDDLGPROC**, envoyant le message WM_INITDIALOG, afin que le fournisseur puisse initialiser les contrôles.</span><span class="sxs-lookup"><span data-stu-id="739fa-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="739fa-157">L’Assistant Profil appelle **SERVICEWIZARDDLGPROC**, envoyant le WIZ_QUERYNUMPAGES message.</span><span class="sxs-lookup"><span data-stu-id="739fa-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="739fa-158">Le fournisseur renvoie le nombre de pages à voir.</span><span class="sxs-lookup"><span data-stu-id="739fa-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="739fa-159">L’Assistant Profil appelle **SERVICEWIZARDDLGPROC**, en envoyant le message WM_COMMAND avec le paramètre  _wParam_ paramétré sur WIZ_NEXT ou WIZ_PREV.</span><span class="sxs-lookup"><span data-stu-id="739fa-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="739fa-160">À ce stade, le fournisseur renvoie false {error} ou révèle ses contrôles et renvoie TRUE {success}.</span><span class="sxs-lookup"><span data-stu-id="739fa-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="739fa-161">Si l’Assistant Profil ID_NEXT, la première page du fournisseur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="739fa-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="739fa-162">Si ID_PREV est transmis, la dernière page s’affiche.</span><span class="sxs-lookup"><span data-stu-id="739fa-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="739fa-163">L’Assistant Profil appelle la fonction **SERVICEWIZARDDLGPROC** du fournisseur, envoyant le message WM_COMMAND avec le paramètre  _wParam_ paramétré sur WIZ_NEXT ou WIZ_PREV (selon le bouton sur lequel l’utilisateur a cliqué).</span><span class="sxs-lookup"><span data-stu-id="739fa-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="739fa-164">Le fournisseur est chargé d’afficher ou de masquer ses contrôles et d’écrire ses données dans **l’IMAPIProp** transmis à l’Assistant Profil pour passer pas à pas dans sa séquence de pages.</span><span class="sxs-lookup"><span data-stu-id="739fa-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="739fa-165">Le fournisseur doit renvoyer TRUE si la page suivante ou précédente a été affichée avec succès, et FALSE si ni la page suivante ni la page précédente ne peuvent être affichées.</span><span class="sxs-lookup"><span data-stu-id="739fa-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="739fa-166">Le fournisseur doit savoir quand il se trouve en dehors de sa séquence de pages et répondre de manière appropriée en masquant ses contrôles et en écrivant ses données dans le profil.</span><span class="sxs-lookup"><span data-stu-id="739fa-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="739fa-167">Si l’utilisateur se place en dehors de la plage de pages du fournisseur, l’Assistant Profil supprime les contrôles masqués du fournisseur de la boîte de dialogue et appelle le fournisseur suivant ou affiche sa page suivante s’il s’agit du dernier fournisseur.</span><span class="sxs-lookup"><span data-stu-id="739fa-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

