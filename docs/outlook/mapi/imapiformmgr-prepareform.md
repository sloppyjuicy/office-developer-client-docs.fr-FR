---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3b10ac5906be0f95930be3bef51fe2d78d583b03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783818"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="0aef1-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="0aef1-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="0aef1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0aef1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0aef1-105">Télécharge un formulaire d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="0aef1-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="0aef1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0aef1-106">Parameters</span></span>

 <span data-ttu-id="0aef1-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0aef1-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="0aef1-108">[in] Un handle vers la fenêtre parent de l’indicateur de progression est affichée pendant que le formulaire est téléchargé.</span><span class="sxs-lookup"><span data-stu-id="0aef1-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="0aef1-109">Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="0aef1-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="0aef1-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0aef1-110">_ulFlags_</span></span>
  
> <span data-ttu-id="0aef1-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont le formulaire est téléchargé.</span><span class="sxs-lookup"><span data-stu-id="0aef1-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="0aef1-112">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="0aef1-112">The following flag can be set:</span></span>
    
<span data-ttu-id="0aef1-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0aef1-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="0aef1-114">Affiche une interface utilisateur pour fournir l’état ou demandez à l’utilisateur pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0aef1-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="0aef1-115">Si cet indicateur n’est pas défini, aucune interface utilisateur est affichée.</span><span class="sxs-lookup"><span data-stu-id="0aef1-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="0aef1-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="0aef1-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="0aef1-117">[in] Pointeur vers un objet d’informations de formulaire pour le formulaire à télécharger.</span><span class="sxs-lookup"><span data-stu-id="0aef1-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0aef1-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="0aef1-118">Return value</span></span>

<span data-ttu-id="0aef1-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0aef1-119">S_OK</span></span> 
  
> <span data-ttu-id="0aef1-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="0aef1-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0aef1-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="0aef1-121">Remarks</span></span>

<span data-ttu-id="0aef1-122">Visionneuses de formulaire appeler la méthode **IMAPIFormMgr::PrepareForm** pour télécharger un formulaire à partir d’un conteneur de formulaire pour l’ouverture.</span><span class="sxs-lookup"><span data-stu-id="0aef1-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="0aef1-123">La plupart des utilisateurs du formulaire est inutile d’appeler **PrepareForm**, car les [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) méthodes et appellent **PrepareForm**, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0aef1-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="0aef1-124">Vous pouvez utiliser **PrepareForm** pour obtenir les bibliothèques de liens dynamiques (DLL) et les autres fichiers associés à un formulaire pour les modifier.</span><span class="sxs-lookup"><span data-stu-id="0aef1-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="0aef1-125">Si le formulaire modifié est chargé dans son conteneur de formulaire, il doit être réinstallé.</span><span class="sxs-lookup"><span data-stu-id="0aef1-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0aef1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aef1-126">See also</span></span>



[<span data-ttu-id="0aef1-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="0aef1-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="0aef1-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="0aef1-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="0aef1-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0aef1-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

