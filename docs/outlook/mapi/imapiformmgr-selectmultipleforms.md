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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b974b733c24e61cb256ac0cf7b377d5630966fdf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579290"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="da4be-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="da4be-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="da4be-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da4be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da4be-105">Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner plusieurs formulaires et renvoie un tableau de formulaire objets informations décrivant les formulaires.</span><span class="sxs-lookup"><span data-stu-id="da4be-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="da4be-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da4be-106">Parameters</span></span>

 <span data-ttu-id="da4be-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="da4be-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="da4be-108">[in] Handle vers la fenêtre parente de la boîte de dialogue qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="da4be-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="da4be-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="da4be-109">_ulFlags_</span></span>
  
> <span data-ttu-id="da4be-110">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes dans le passé.</span><span class="sxs-lookup"><span data-stu-id="da4be-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="da4be-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="da4be-111">The following flag can be set:</span></span>
    
<span data-ttu-id="da4be-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="da4be-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="da4be-113">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="da4be-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="da4be-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="da4be-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="da4be-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="da4be-115">_pszTitle_</span></span>
  
> <span data-ttu-id="da4be-116">[in] Pointeur vers une chaîne qui contient la légende de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="da4be-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="da4be-117">Si le paramètre _pszTitle_ est NULL, le fournisseur de bibliothèque de formulaires qui fournit les formulaires fournit une légende par défaut.</span><span class="sxs-lookup"><span data-stu-id="da4be-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="da4be-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="da4be-118">_pfld_</span></span>
  
> <span data-ttu-id="da4be-119">[in] Pointeur vers le dossier à partir desquels sélectionner les formulaires.</span><span class="sxs-lookup"><span data-stu-id="da4be-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="da4be-120">Si le paramètre _pfld_ est NULL, les formulaires sont sélectionnées dans le conteneur de formulaire local, personnel ou organisation.</span><span class="sxs-lookup"><span data-stu-id="da4be-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="da4be-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="da4be-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="da4be-122">[in] Pointeur vers un tableau d’objets d’informations de formulaire qui sont présélectionnés pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="da4be-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="da4be-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="da4be-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="da4be-124">[out] Pointeur vers un pointeur vers le tableau d’objets formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="da4be-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da4be-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="da4be-125">Return value</span></span>

<span data-ttu-id="da4be-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="da4be-126">S_OK</span></span> 
  
> <span data-ttu-id="da4be-127">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="da4be-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="da4be-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="da4be-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="da4be-129">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="da4be-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="da4be-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="da4be-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="da4be-131">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="da4be-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="da4be-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="da4be-132">Remarks</span></span>

<span data-ttu-id="da4be-133">Visionneuses de formulaire appellent la méthode de **IMAPIFormMgr::SelectMultipleForms** au premier présente une boîte de dialogue qui permet à l’utilisateur de sélectionner plusieurs formulaires et puis pour récupérer un tableau de formulaire d’informations des objets qui décrivent les formulaires sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="da4be-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="da4be-134">La boîte de dialogue **SelectMultipleForms** affiche tous les formulaires, si elles sont masquées (autrement dit, si leurs propriétés masquées sont claires).</span><span class="sxs-lookup"><span data-stu-id="da4be-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="da4be-135">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="da4be-135">Notes to implementers</span></span>

<span data-ttu-id="da4be-136">Si une visionneuse de formulaire transmet l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes sont en Unicode.</span><span class="sxs-lookup"><span data-stu-id="da4be-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="da4be-137">Fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé.</span><span class="sxs-lookup"><span data-stu-id="da4be-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="da4be-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da4be-138">See also</span></span>



[<span data-ttu-id="da4be-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="da4be-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

