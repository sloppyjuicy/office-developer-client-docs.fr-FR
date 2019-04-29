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
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="8b2c0-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="8b2c0-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="8b2c0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b2c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b2c0-105">Télécharge un formulaire à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="8b2c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b2c0-106">Parameters</span></span>

 <span data-ttu-id="8b2c0-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8b2c0-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="8b2c0-108">dans Handle de la fenêtre parente de l'indicateur de progression qui est affiché pendant le téléchargement du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="8b2c0-109">Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="8b2c0-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="8b2c0-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8b2c0-110">_ulFlags_</span></span>
  
> <span data-ttu-id="8b2c0-111">dans Masque de des indicateurs qui contrôle le mode de téléchargement du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="8b2c0-112">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="8b2c0-112">The following flag can be set:</span></span>
    
<span data-ttu-id="8b2c0-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="8b2c0-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="8b2c0-114">Affiche une interface utilisateur pour fournir l'État ou inviter l'utilisateur à fournir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="8b2c0-115">Si cet indicateur n'est pas défini, aucune interface utilisateur n'est affichée.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="8b2c0-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="8b2c0-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="8b2c0-117">dans Pointeur vers un objet d'informations de formulaire pour le formulaire à télécharger.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8b2c0-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b2c0-118">Return value</span></span>

<span data-ttu-id="8b2c0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b2c0-119">S_OK</span></span> 
  
> <span data-ttu-id="8b2c0-120">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b2c0-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b2c0-121">Remarks</span></span>

<span data-ttu-id="8b2c0-122">Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::P repareform** pour télécharger un formulaire à partir d'un conteneur de formulaire pour l'ouvrir.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="8b2c0-123">La plupart des visionneuses de formulaires n'ont pas besoin d'appeler **PrepareForm**, car les méthodes [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) et [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) appellent **PrepareForm**, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="8b2c0-124">Vous pouvez utiliser **PrepareForm** pour obtenir les bibliothèques de liens dynamiques (dll) et les autres fichiers associés à un formulaire afin de les modifier.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="8b2c0-125">Si le formulaire modifié est chargé à nouveau dans son conteneur de formulaire, il doit être réinstallé.</span><span class="sxs-lookup"><span data-stu-id="8b2c0-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b2c0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b2c0-126">See also</span></span>



[<span data-ttu-id="8b2c0-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="8b2c0-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="8b2c0-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="8b2c0-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="8b2c0-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b2c0-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

