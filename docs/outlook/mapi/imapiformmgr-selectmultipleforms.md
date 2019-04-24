---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321594"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="3275e-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="3275e-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="3275e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3275e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3275e-105">Affiche une boîte de dialogue qui permet à l'utilisateur de sélectionner plusieurs formulaires et renvoie un tableau d'objets d'informations de formulaire qui décrivent ces formulaires.</span><span class="sxs-lookup"><span data-stu-id="3275e-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="3275e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3275e-106">Parameters</span></span>

 <span data-ttu-id="3275e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3275e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="3275e-108">dans Handle de la fenêtre parent de la boîte de dialogue affichée.</span><span class="sxs-lookup"><span data-stu-id="3275e-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="3275e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3275e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3275e-110">dans Masque de bits des indicateurs qui contrôle le type des chaînes transmises.</span><span class="sxs-lookup"><span data-stu-id="3275e-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="3275e-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="3275e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3275e-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3275e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3275e-113">Les chaînes transmises sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="3275e-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="3275e-114">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="3275e-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3275e-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="3275e-115">_pszTitle_</span></span>
  
> <span data-ttu-id="3275e-116">dans Pointeur vers une chaîne qui contient la légende de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="3275e-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="3275e-117">Si le paramètre _pszTitle_ est null, le fournisseur de bibliothèque de formulaires qui fournit les formulaires fournit une légende par défaut.</span><span class="sxs-lookup"><span data-stu-id="3275e-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="3275e-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="3275e-118">_pfld_</span></span>
  
> <span data-ttu-id="3275e-119">dans Pointeur vers le dossier à partir duquel sélectionner les formulaires.</span><span class="sxs-lookup"><span data-stu-id="3275e-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="3275e-120">Si le paramètre _pfld_ est null, les formulaires sont sélectionnés à partir du conteneur de formulaire local, personnel ou organisation.</span><span class="sxs-lookup"><span data-stu-id="3275e-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="3275e-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="3275e-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="3275e-122">dans Pointeur vers un tableau d'objets d'informations de formulaire présélectionnés pour l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3275e-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="3275e-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="3275e-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="3275e-124">remarquer Pointeur vers un pointeur vers le tableau renvoyé d'objets d'informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="3275e-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3275e-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3275e-125">Return value</span></span>

<span data-ttu-id="3275e-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="3275e-126">S_OK</span></span> 
  
> <span data-ttu-id="3275e-127">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="3275e-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="3275e-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3275e-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3275e-129">L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="3275e-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="3275e-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="3275e-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="3275e-131">L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="3275e-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3275e-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="3275e-132">Remarks</span></span>

<span data-ttu-id="3275e-133">Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr:: SelectMultipleForms** pour commencer par présenter une boîte de dialogue qui permet à l'utilisateur de sélectionner plusieurs formulaires, puis de récupérer un tableau d'objets d'informations de formulaire qui décrivent les formulaires sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="3275e-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="3275e-134">La boîte de dialogue **SelectMultipleForms** affiche tous les formulaires, qu'ils soient ou non masqués (c'est-à-dire, si leurs propriétés masquées sont claires ou non).</span><span class="sxs-lookup"><span data-stu-id="3275e-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3275e-135">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="3275e-135">Notes to implementers</span></span>

<span data-ttu-id="3275e-136">Si une visionneuse de formulaires transmet l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="3275e-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="3275e-137">Les fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est transmis.</span><span class="sxs-lookup"><span data-stu-id="3275e-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3275e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3275e-138">See also</span></span>



[<span data-ttu-id="3275e-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3275e-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

