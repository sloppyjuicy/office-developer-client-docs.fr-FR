---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f66d0fb1fc9d252ff8b6985c4a54de79313266d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577925"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="6e857-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="6e857-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="6e857-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e857-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e857-105">Présente une boîte de dialogue qui permet à l’utilisateur sélectionner un conteneur de formulaire et renvoie une interface pour l’objet conteneur de l’utilisateur sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6e857-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="6e857-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e857-106">Parameters</span></span>

 <span data-ttu-id="6e857-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6e857-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="6e857-108">[in] Handle vers la fenêtre parente de la boîte de dialogue qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6e857-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="6e857-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6e857-109">_ulFlags_</span></span>
  
> <span data-ttu-id="6e857-110">[in] Un masque de bits d’indicateurs qui contrôle la façon dont la bibliothèque de formulaires est activée (autrement dit, comment le conteneur de formulaire est sélectionné).</span><span class="sxs-lookup"><span data-stu-id="6e857-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="6e857-111">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="6e857-111">The following flags can be set:</span></span>
    
<span data-ttu-id="6e857-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="6e857-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="6e857-113">Effectuer une sélection à partir de tous les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="6e857-113">Selection can be made from all containers.</span></span> <span data-ttu-id="6e857-114">Il s’agit du type de sélection par défaut.</span><span class="sxs-lookup"><span data-stu-id="6e857-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="6e857-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="6e857-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="6e857-116">Sélection peut être effectuée qu’à partir de conteneurs de dossiers.</span><span class="sxs-lookup"><span data-stu-id="6e857-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="6e857-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="6e857-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="6e857-118">Sélection peut être effectuée qu’à partir de conteneurs qui ne sont pas associés à des dossiers.</span><span class="sxs-lookup"><span data-stu-id="6e857-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="6e857-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="6e857-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="6e857-120">[out] Pointeur vers un pointeur vers l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="6e857-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="6e857-121">Cette interface n’est pour l’objet conteneur qui est sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6e857-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6e857-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6e857-122">Return value</span></span>

<span data-ttu-id="6e857-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e857-123">S_OK</span></span> 
  
> <span data-ttu-id="6e857-124">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6e857-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e857-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e857-125">Remarks</span></span>

<span data-ttu-id="6e857-126">En général, les visionneuses de formulaire appelez la méthode **IMAPIFormMgr::SelectFormContainer** pour sélectionner un conteneur de formulaire dans lequel un formulaire est installé.</span><span class="sxs-lookup"><span data-stu-id="6e857-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="6e857-127">**SelectFormContainer** ne peut pas être utilisée pour sélectionner le conteneur de formulaire local, qui a la valeur HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="6e857-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6e857-128">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6e857-128">MFCMAPI reference</span></span>

<span data-ttu-id="6e857-129">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6e857-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6e857-130">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6e857-130">**File**</span></span>|<span data-ttu-id="6e857-131">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6e857-131">**Function**</span></span>|<span data-ttu-id="6e857-132">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6e857-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6e857-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6e857-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="6e857-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="6e857-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="6e857-135">MFCMAPI utilise la méthode **IMAPIFormMgr::SelectFormContainer** pour sélectionner un conteneur de formulaire avant l’affichage de son contenu.</span><span class="sxs-lookup"><span data-stu-id="6e857-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e857-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e857-136">See also</span></span>



[<span data-ttu-id="6e857-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e857-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="6e857-138">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6e857-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

