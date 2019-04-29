---
title: IMAPIFormContainerInstallForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.InstallForm
api_type:
- COM
ms.assetid: b39ca52c-4dbe-41c0-9e1b-3998a9dc9742
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a0650033e4fea79046eac5757e3d0deb963c38e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405085"
---
# <a name="imapiformcontainerinstallform"></a><span data-ttu-id="6e99d-103">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="6e99d-103">IMAPIFormContainer::InstallForm</span></span>

  
  
<span data-ttu-id="6e99d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e99d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e99d-105">Installe un formulaire dans une bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="6e99d-105">Installs a form into a form library.</span></span>
  
```cpp
HRESULT InstallForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR szCfgPathName
);
```

## <a name="parameters"></a><span data-ttu-id="6e99d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e99d-106">Parameters</span></span>

 <span data-ttu-id="6e99d-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6e99d-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="6e99d-108">dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche.</span><span class="sxs-lookup"><span data-stu-id="6e99d-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="6e99d-109">Le paramètre _ulUIParam_ est ignoré sauf si l'application cliente définit l'indicateur MAPI_DIALOG dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="6e99d-109">The  _ulUIParam_ parameter is ignored unless the client application sets the MAPI_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="6e99d-110">Le paramètre _ulUIParam_ peut être null si MAPI_DIALOG n'est pas également passé.</span><span class="sxs-lookup"><span data-stu-id="6e99d-110">The  _ulUIParam_ parameter can be NULL if MAPI_DIALOG is not also passed.</span></span> 
    
 <span data-ttu-id="6e99d-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6e99d-111">_ulFlags_</span></span>
  
> <span data-ttu-id="6e99d-112">dans Masque de des indicateurs qui contrôle l'installation du formulaire.</span><span class="sxs-lookup"><span data-stu-id="6e99d-112">[in] A bitmask of flags that controls the installation of the form.</span></span> <span data-ttu-id="6e99d-113">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="6e99d-113">The following flags can be set:</span></span>
    
<span data-ttu-id="6e99d-114">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6e99d-114">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6e99d-115">Affiche une boîte de dialogue qui fournit des informations d'avancement ou invite l'utilisateur à fournir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6e99d-115">Displays a dialog box to provide progress information or prompt the user for more information.</span></span> <span data-ttu-id="6e99d-116">Si cet indicateur n'est pas défini, aucune boîte de dialogue ne s'affiche.</span><span class="sxs-lookup"><span data-stu-id="6e99d-116">If this flag is not set, no dialog box is displayed.</span></span>
    
<span data-ttu-id="6e99d-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6e99d-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6e99d-118">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="6e99d-118">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="6e99d-119">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="6e99d-119">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
<span data-ttu-id="6e99d-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span><span class="sxs-lookup"><span data-stu-id="6e99d-120">MAPIFORM_INSTALL_OVERWRITEONCONFLICT</span></span> 
  
> <span data-ttu-id="6e99d-121">S'il existe déjà un autre formulaire qui gère la classe de message gérée par ce formulaire, remplacez le formulaire existant par celui-ci.</span><span class="sxs-lookup"><span data-stu-id="6e99d-121">If another form already exists that handles the message class handled by this form, replace the existing form with this one.</span></span> <span data-ttu-id="6e99d-122">Cet indicateur est ignoré si l'indicateur MAPI_DIALOG est également présent.</span><span class="sxs-lookup"><span data-stu-id="6e99d-122">This flag is ignored if the MAPI_DIALOG flag is also present.</span></span> 
    
 <span data-ttu-id="6e99d-123">_szCfgPathName_</span><span class="sxs-lookup"><span data-stu-id="6e99d-123">_szCfgPathName_</span></span>
  
> <span data-ttu-id="6e99d-124">dans Chemin d'accès au fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="6e99d-124">[in] The path to the form's configuration file.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6e99d-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6e99d-125">Return value</span></span>

<span data-ttu-id="6e99d-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e99d-126">S_OK</span></span> 
  
> <span data-ttu-id="6e99d-127">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6e99d-127">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6e99d-128">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="6e99d-128">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="6e99d-129">Une erreur d'implémentation s'est produite.</span><span class="sxs-lookup"><span data-stu-id="6e99d-129">An implementation error occurred.</span></span> <span data-ttu-id="6e99d-130">Pour obtenir la structure [MAPIERROR](mapierror.md) associée à l'erreur, appelez la méthode [IMAPIFormContainer:: GetLastError](imapiformcontainer-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6e99d-130">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="6e99d-131">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="6e99d-131">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="6e99d-132">L'utilisateur a annulé l'installation du formulaire, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6e99d-132">The user canceled the installation of the form, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="6e99d-133">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="6e99d-133">Notes to implementers</span></span>

<span data-ttu-id="6e99d-134">Les fournisseurs de bibliothèques de formulaires doivent remplir une structure **MAPIERROR** et renvoyer MAPI_E_EXTENDED_ERROR si l'une des conditions suivantes se produit:</span><span class="sxs-lookup"><span data-stu-id="6e99d-134">Form library providers should fill in a **MAPIERROR** structure and return MAPI_E_EXTENDED_ERROR if any of the following conditions occur:</span></span> 
  
- <span data-ttu-id="6e99d-135">Le fichier de configuration est introuvable.</span><span class="sxs-lookup"><span data-stu-id="6e99d-135">The configuration file is not found.</span></span>
    
- <span data-ttu-id="6e99d-136">Le fichier de configuration n'est pas lisible.</span><span class="sxs-lookup"><span data-stu-id="6e99d-136">The configuration file is not readable.</span></span>
    
- <span data-ttu-id="6e99d-137">Le fichier de configuration n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6e99d-137">The configuration file is invalid.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="6e99d-138">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="6e99d-138">Notes to callers</span></span>

<span data-ttu-id="6e99d-139">Les applications clientes appellent la méthode **IMAPIFormContainer:: InstallForm** pour installer un formulaire dans un conteneur de formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="6e99d-139">Client applications call the **IMAPIFormContainer::InstallForm** method to install a form into a specific form container.</span></span> <span data-ttu-id="6e99d-140">Le paramètre _szCfgPathName_ doit contenir le chemin d'accès d'un fichier de configuration de formulaire (c'est-à-dire un fichier doté de l'extension. cfg qui décrit le formulaire et son implémentation).</span><span class="sxs-lookup"><span data-stu-id="6e99d-140">The  _szCfgPathName_ parameter must contain the path of a form configuration file (that is, a file with the .cfg extension that describes the form and its implementation).</span></span> <span data-ttu-id="6e99d-141">Les indicateurs dans le paramètre _ulFlags_ spécifient les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="6e99d-141">The flags in the  _ulFlags_ parameter specify the following:</span></span> 
  
- <span data-ttu-id="6e99d-142">Si l'indicateur MAPI_DIALOG est défini, une interface utilisateur s'affiche, ce qui permet à l'utilisateur qui installe le formulaire de spécifier les détails de l'installation.</span><span class="sxs-lookup"><span data-stu-id="6e99d-142">If the MAPI_DIALOG flag is set, a user interface is displayed, enabling the user who is installing the form to specify installation details.</span></span>
    
- <span data-ttu-id="6e99d-143">Si l'indicateur MAPIFORM_INSTALL_OVERWRITEONCONFLICT est défini, tout formulaire précédent pour la même classe de message est remplacé par le formulaire en cours d'installation.</span><span class="sxs-lookup"><span data-stu-id="6e99d-143">If the MAPIFORM_INSTALL_OVERWRITEONCONFLICT flag is set, any previous form for the same message class is replaced with the form being installed.</span></span> <span data-ttu-id="6e99d-144">Dans le cas contraire, l'installation du formulaire est fusionnée avec la description de formulaire actuelle, si elle existe.</span><span class="sxs-lookup"><span data-stu-id="6e99d-144">Otherwise, the form installation is merged with the current form description, if one exists.</span></span>
    
- <span data-ttu-id="6e99d-145">Si MAPI_DIALOG est défini, MAPIFORM_INSTALL_OVERWRITEONCONFLICT est ignoré.</span><span class="sxs-lookup"><span data-stu-id="6e99d-145">If MAPI_DIALOG is set, MAPIFORM_INSTALL_OVERWRITEONCONFLICT is ignored.</span></span>
    
- <span data-ttu-id="6e99d-146">L'absence de MAPIFORM_INSTALL_OVERWRITEONCONFLICT dans l'ensemble d'indicateurs signifie qu'une fusion sera réalisée.</span><span class="sxs-lookup"><span data-stu-id="6e99d-146">The absence of MAPIFORM_INSTALL_OVERWRITEONCONFLICT in the flag set means that a merge will be done.</span></span> <span data-ttu-id="6e99d-147">Toutes les nouvelles plateformes du fichier. cfg qui ne sont pas présentes dans la description du formulaire sont installées et aucune autre modification n'est effectuée.</span><span class="sxs-lookup"><span data-stu-id="6e99d-147">Any new platforms in the .cfg file that are not currently present in the form description will be installed and no other changes will occur.</span></span>
    
- <span data-ttu-id="6e99d-148">Si l'indicateur MAPI_UNICODE est défini, le chemin d'accès au fichier de configuration du formulaire est une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="6e99d-148">If the MAPI_UNICODE flag is set, the path of the form configuration file is a Unicode string.</span></span> 
    
<span data-ttu-id="6e99d-149">Les clients doivent appeler [IMAPIFormContainer:: GetLastError](imapiformcontainer-getlasterror.md) si **InstallForm** renvoie MAPI_E_EXTENDED_ERROR et vérifier la structure [MAPIERROR](mapierror.md) renvoyée pour déterminer la condition à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="6e99d-149">Clients should call [IMAPIFormContainer::GetLastError](imapiformcontainer-getlasterror.md) if **InstallForm** returns MAPI_E_EXTENDED_ERROR, and they should check the returned [MAPIERROR](mapierror.md) structure to determine the condition that raised the error.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6e99d-150">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6e99d-150">MFCMAPI reference</span></span>

<span data-ttu-id="6e99d-151">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6e99d-151">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6e99d-152">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6e99d-152">**File**</span></span>|<span data-ttu-id="6e99d-153">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6e99d-153">**Function**</span></span>|<span data-ttu-id="6e99d-154">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6e99d-154">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6e99d-155">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="6e99d-155">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="6e99d-156">CFormContainerDlg:: OnInstallForm</span><span class="sxs-lookup"><span data-stu-id="6e99d-156">CFormContainerDlg::OnInstallForm</span></span>  <br/> |<span data-ttu-id="6e99d-157">MFCMAPI utilise la méthode **IMAPIFormContainer:: InstallForm** pour installer un formulaire dans un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="6e99d-157">MFCMAPI uses the **IMAPIFormContainer::InstallForm** method to install a form in a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e99d-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e99d-158">See also</span></span>



[<span data-ttu-id="6e99d-159">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="6e99d-159">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="6e99d-160">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e99d-160">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="6e99d-161">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6e99d-161">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

