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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416649"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="78315-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="78315-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="78315-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78315-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78315-105">Télécharge un formulaire à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="78315-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="78315-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78315-106">Parameters</span></span>

 <span data-ttu-id="78315-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="78315-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="78315-108">[in] Handle vers la fenêtre parent de l’indicateur de progression qui s’affiche pendant le téléchargement du formulaire.</span><span class="sxs-lookup"><span data-stu-id="78315-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="78315-109">Le _paramètre ulUIParam_ est ignoré, sauf si l’MAPI_DIALOG est définie dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="78315-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="78315-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78315-110">_ulFlags_</span></span>
  
> <span data-ttu-id="78315-111">[in] Masque de bits d’indicateurs qui contrôle le mode de téléchargement du formulaire.</span><span class="sxs-lookup"><span data-stu-id="78315-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="78315-112">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="78315-112">The following flag can be set:</span></span>
    
<span data-ttu-id="78315-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="78315-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="78315-114">Affiche une interface utilisateur pour fournir un état ou invite l’utilisateur à fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="78315-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="78315-115">Si cet indicateur n’est pas définie, aucune interface utilisateur n’est affichée.</span><span class="sxs-lookup"><span data-stu-id="78315-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="78315-116">_pfinfo_</span><span class="sxs-lookup"><span data-stu-id="78315-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="78315-117">[in] Pointeur vers un objet d’informations de formulaire pour le formulaire à télécharger.</span><span class="sxs-lookup"><span data-stu-id="78315-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78315-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="78315-118">Return value</span></span>

<span data-ttu-id="78315-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="78315-119">S_OK</span></span> 
  
> <span data-ttu-id="78315-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="78315-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78315-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="78315-121">Remarks</span></span>

<span data-ttu-id="78315-122">Les visionneuses de formulaire appellent la méthode **IMAPIFormMgr::P repareForm** pour télécharger un formulaire à partir d’un conteneur de formulaire à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="78315-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="78315-123">La plupart des visionneuses de formulaires n’ont pas besoin d’appeler **PrepareForm,** car les deux méthodes [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) et [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) appellent **PrepareForm,** si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="78315-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="78315-124">Vous pouvez utiliser **PrepareForm** pour obtenir les bibliothèques de liens dynamiques (DLL) et d’autres fichiers associés à un formulaire pour les modifier.</span><span class="sxs-lookup"><span data-stu-id="78315-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="78315-125">Si le formulaire modifié est chargé à nouveau dans son conteneur de formulaire, il doit être réinstallé.</span><span class="sxs-lookup"><span data-stu-id="78315-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78315-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78315-126">See also</span></span>



[<span data-ttu-id="78315-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="78315-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="78315-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="78315-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="78315-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78315-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

