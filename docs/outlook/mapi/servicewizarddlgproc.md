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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 649046aa48f293caa5bd71cc670481b5c205459a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787137"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="712c8-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="712c8-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="712c8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="712c8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="712c8-105">Définit une fonction de rappel appelée par l’Assistant profil pour autoriser un fournisseur de services de réagir aux événements utilisateur lorsque les feuilles de propriétés ou des pages du fournisseur sont affichés.</span><span class="sxs-lookup"><span data-stu-id="712c8-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="712c8-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="712c8-106">Header file:</span></span>  <br/> |<span data-ttu-id="712c8-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="712c8-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="712c8-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="712c8-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="712c8-109">Fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="712c8-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="712c8-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="712c8-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="712c8-111">Assistant profil MAPI</span><span class="sxs-lookup"><span data-stu-id="712c8-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="712c8-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="712c8-112">Parameters</span></span>

<span data-ttu-id="712c8-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="712c8-113">_hDlg_</span></span>
  
> <span data-ttu-id="712c8-114">[in] Handle de fenêtre pour la boîte de dialogue Assistant profil.</span><span class="sxs-lookup"><span data-stu-id="712c8-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="712c8-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="712c8-115">_wMsgID_</span></span>
  
> <span data-ttu-id="712c8-116">[in] Le message de fenêtre à traiter.</span><span class="sxs-lookup"><span data-stu-id="712c8-116">[in] The window message to be processed.</span></span> <span data-ttu-id="712c8-117">Outre les messages de fenêtre normale attendus par une boîte de dialogue modale, les messages suivants peuvent être reçus :</span><span class="sxs-lookup"><span data-stu-id="712c8-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="712c8-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="712c8-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="712c8-119">L’Assistant profil est terminée.</span><span class="sxs-lookup"><span data-stu-id="712c8-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="712c8-120">Le fournisseur de services doit faire tout le nettoyage requis tels que les libérer dynamiquement de mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="712c8-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="712c8-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="712c8-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="712c8-122">Un des contrôles du fournisseur a été sélectionné, ou le bouton **suivant** ou **précédent** a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="712c8-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="712c8-123">La valeur du paramètre _wParam_ indique lequel de ces événements utilisateur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="712c8-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="712c8-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="712c8-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="712c8-125">L’utilisateur a déplacé vers une autre page de propriétés, dont la boîte de dialogue doit être initialisée.</span><span class="sxs-lookup"><span data-stu-id="712c8-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="712c8-126">Le fournisseur doit initialiser les contrôles de l’Assistant profil a ajouté à la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="712c8-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="712c8-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="712c8-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="712c8-128">L’Assistant profil demande le nombre de pages que le fournisseur doit afficher.</span><span class="sxs-lookup"><span data-stu-id="712c8-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="712c8-129">Le fournisseur doit renvoyer le nombre de pages au lieu de la valeur TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="712c8-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="712c8-130">Par exemple, utilisez l’instruction suivante de retour pour indiquer que trois pages doivent être affichée :</span><span class="sxs-lookup"><span data-stu-id="712c8-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="712c8-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="712c8-131">_wParam_</span></span>
  
> <span data-ttu-id="712c8-132">[in] Un paramètre de 32 bits associé à des messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="712c8-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="712c8-133">Le message spécifié dans le paramètre _wMsgID_ dépendent de valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="712c8-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="712c8-134">Outre les valeurs prévus avec les messages de fenêtre normale pour une boîte de dialogue modale, les valeurs suivantes peuvent être reçus :</span><span class="sxs-lookup"><span data-stu-id="712c8-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="712c8-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="712c8-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="712c8-136">Lorsque _wMsgID_ contient WM_COMMAND, l’utilisateur a cliqué sur le bouton **suivant** .</span><span class="sxs-lookup"><span data-stu-id="712c8-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="712c8-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="712c8-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="712c8-138">Lorsque _wMsgID_ contient WM_COMMAND, l’utilisateur a cliqué sur le bouton **précédent** .</span><span class="sxs-lookup"><span data-stu-id="712c8-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="712c8-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="712c8-139">_lParam_</span></span>
  
> <span data-ttu-id="712c8-140">[in] Un paramètre de 32 bits associé à des messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="712c8-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="712c8-141">Le message spécifié dans le paramètre _wMsgID_ dépendent de valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="712c8-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="712c8-142">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="712c8-142">Return value</span></span>

<span data-ttu-id="712c8-143">La valeur renvoyée par une fonction **SERVICEWIZARDDLGPROC** en fonction de dépend de la fenêtre message reçu.</span><span class="sxs-lookup"><span data-stu-id="712c8-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="712c8-144">Notez en particulier que les exceptionnelles renvoient la valeur pour le message WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="712c8-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="712c8-145">Les valeurs de retour normales sont :</span><span class="sxs-lookup"><span data-stu-id="712c8-145">The normal return values are:</span></span> 
  
<span data-ttu-id="712c8-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="712c8-146">TRUE</span></span> 
  
> <span data-ttu-id="712c8-147">Le fournisseur de services a traité le message reçu.</span><span class="sxs-lookup"><span data-stu-id="712c8-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="712c8-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="712c8-148">FALSE</span></span> 
  
> <span data-ttu-id="712c8-149">Le fournisseur de services n’a pas traité le message reçu.</span><span class="sxs-lookup"><span data-stu-id="712c8-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="712c8-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="712c8-150">Remarks</span></span>

<span data-ttu-id="712c8-151">Lorsque l’utilisateur passe d’une page de propriété à une autre, le fournisseur est chargé de masquer les contrôles de la page ancienne et affiche les contrôles de la page suivante ou précédente.</span><span class="sxs-lookup"><span data-stu-id="712c8-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="712c8-152">Lorsque l’utilisateur clique sur le bouton **suivant** , la fonction **SERVICEWIZARDDLGPROC** en fonction est appelée avec le message WM_COMMAND et WIZ_NEXT dans le paramètre _wParam_ .</span><span class="sxs-lookup"><span data-stu-id="712c8-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="712c8-153">Les étapes suivantes décrivent ce qui se produit entre le temps que l’utilisateur clique sur **suivant** et lors du rendu des pages de configuration du premier fournisseur.</span><span class="sxs-lookup"><span data-stu-id="712c8-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="712c8-154">L’Assistant profil masquer tous les contrôles qui se trouvent dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="712c8-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="712c8-155">L’Assistant profil ajoute les contrôles masqués du fournisseur à la page.</span><span class="sxs-lookup"><span data-stu-id="712c8-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="712c8-156">L’Assistant profil appelle **SERVICEWIZARDDLGPROC**, envoyer le message WM_INITDIALOG, afin que le fournisseur peut initialiser les contrôles.</span><span class="sxs-lookup"><span data-stu-id="712c8-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="712c8-157">L’Assistant profil appelle **SERVICEWIZARDDLGPROC**, l’envoi du message WIZ_QUERYNUMPAGES.</span><span class="sxs-lookup"><span data-stu-id="712c8-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="712c8-158">Le fournisseur renvoie le nombre de pages à afficher.</span><span class="sxs-lookup"><span data-stu-id="712c8-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="712c8-159">L’Assistant profil appelle **SERVICEWIZARDDLGPROC**, envoyer le message WM_COMMAND avec le paramètre _wParam_ défini sur WIZ_NEXT ou WIZ_PREV.</span><span class="sxs-lookup"><span data-stu-id="712c8-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="712c8-160">À ce stade, le fournisseur soit renvoie la valeur FALSE {erreur} ou révèle ses contrôles et renvoie la valeur TRUE {réussite}.</span><span class="sxs-lookup"><span data-stu-id="712c8-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="712c8-161">Si l’Assistant profil passe ID_NEXT, la première page du fournisseur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="712c8-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="712c8-162">Si ID_PREV est passé, la dernière page s’affiche.</span><span class="sxs-lookup"><span data-stu-id="712c8-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="712c8-163">L’Assistant profil appelle fonction **SERVICEWIZARDDLGPROC** du fournisseur d’envoyer le message WM_COMMAND avec le paramètre _wParam_ défini sur WIZ_NEXT ou WIZ_PREV (selon le bouton sur lequel l’utilisateur a cliqué).</span><span class="sxs-lookup"><span data-stu-id="712c8-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="712c8-164">Le fournisseur est responsable de l’affichage ou masquage de ses contrôles et écriture de ses données dans **IMAPIProp** passé à l’Assistant profil afin de parcourir la séquence de pages.</span><span class="sxs-lookup"><span data-stu-id="712c8-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="712c8-165">Le fournisseur doit retourner la valeur TRUE si la page suivante ou précédente a été correctement affichée, et FALSE si ni la page suivante ou précédente peut être affichée.</span><span class="sxs-lookup"><span data-stu-id="712c8-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="712c8-166">Le fournisseur doit tenir compte lorsqu’il est pas en dehors de la séquence de pages et répondre de façon appropriée en masquant ses contrôles et en écriture de ses données dans le profil.</span><span class="sxs-lookup"><span data-stu-id="712c8-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="712c8-167">Si les étapes de l’utilisateur en dehors de la plage du fournisseur de pages, l’Assistant profil supprime les contrôles masqués du fournisseur de la boîte de dialogue et appelle le fournisseur suivant ou affiche la page suivante, si c’était le dernier fournisseur.</span><span class="sxs-lookup"><span data-stu-id="712c8-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

