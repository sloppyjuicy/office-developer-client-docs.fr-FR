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
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428591"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="f52b8-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="f52b8-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="f52b8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f52b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f52b8-105">Présente une boîte de dialogue qui permet à l’utilisateur de sélectionner un conteneur de formulaires et renvoie une interface pour l’objet conteneur sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f52b8-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="f52b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f52b8-106">Parameters</span></span>

 <span data-ttu-id="f52b8-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f52b8-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f52b8-108">[in] Poignée vers la fenêtre parente de la boîte de dialogue affichée.</span><span class="sxs-lookup"><span data-stu-id="f52b8-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="f52b8-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f52b8-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f52b8-110">[in] Masque de bits d’indicateurs qui contrôle la façon dont la bibliothèque de formulaires est sélectionnée (autrement dit, la façon dont le conteneur de formulaire est sélectionné).</span><span class="sxs-lookup"><span data-stu-id="f52b8-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="f52b8-111">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="f52b8-111">The following flags can be set:</span></span>
    
<span data-ttu-id="f52b8-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="f52b8-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="f52b8-113">La sélection peut être réalisée à partir de tous les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="f52b8-113">Selection can be made from all containers.</span></span> <span data-ttu-id="f52b8-114">Il s’agit du type de sélection par défaut.</span><span class="sxs-lookup"><span data-stu-id="f52b8-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="f52b8-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="f52b8-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="f52b8-116">La sélection ne peut être réalisée qu’à partir de conteneurs de dossiers.</span><span class="sxs-lookup"><span data-stu-id="f52b8-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="f52b8-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="f52b8-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="f52b8-118">La sélection ne peut être réalisée qu’à partir de conteneurs qui ne sont pas associés à des dossiers.</span><span class="sxs-lookup"><span data-stu-id="f52b8-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="f52b8-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="f52b8-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="f52b8-120">[out] Pointeur vers un pointeur vers l’interface renvoyée.</span><span class="sxs-lookup"><span data-stu-id="f52b8-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="f52b8-121">Cette interface est pour l’objet conteneur sélectionné par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f52b8-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f52b8-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f52b8-122">Return value</span></span>

<span data-ttu-id="f52b8-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="f52b8-123">S_OK</span></span> 
  
> <span data-ttu-id="f52b8-124">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f52b8-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f52b8-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="f52b8-125">Remarks</span></span>

<span data-ttu-id="f52b8-126">Les visionneuses de formulaire appellent généralement la méthode **IMAPIFormMgr::SelectFormContainer** pour sélectionner un conteneur de formulaire dans lequel un formulaire est installé.</span><span class="sxs-lookup"><span data-stu-id="f52b8-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="f52b8-127">**SelectFormContainer ne peut** pas être utilisé pour sélectionner le conteneur de formulaire local, dont la valeur est HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="f52b8-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f52b8-128">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f52b8-128">MFCMAPI reference</span></span>

<span data-ttu-id="f52b8-129">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f52b8-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f52b8-130">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f52b8-130">**File**</span></span>|<span data-ttu-id="f52b8-131">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f52b8-131">**Function**</span></span>|<span data-ttu-id="f52b8-132">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f52b8-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f52b8-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f52b8-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="f52b8-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="f52b8-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="f52b8-135">MFCMAPI utilise la méthode **IMAPIFormMgr::SelectFormContainer** pour sélectionner un conteneur de formulaire avant d’en rendre le contenu.</span><span class="sxs-lookup"><span data-stu-id="f52b8-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f52b8-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f52b8-136">See also</span></span>



[<span data-ttu-id="f52b8-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f52b8-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="f52b8-138">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f52b8-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

