---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432582"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="859f2-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="859f2-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="859f2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="859f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="859f2-105">Récupère un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="859f2-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="859f2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="859f2-106">Parameters</span></span>

 <span data-ttu-id="859f2-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="859f2-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="859f2-108">[in] Handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="859f2-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="859f2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="859f2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="859f2-110">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet de progression doit calculer la progression.</span><span class="sxs-lookup"><span data-stu-id="859f2-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="859f2-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="859f2-111">The following flag can be set:</span></span>
    
<span data-ttu-id="859f2-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="859f2-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="859f2-113">La progression est calculée pour un élément de niveau supérieur, tel qu’un dossier parent.</span><span class="sxs-lookup"><span data-stu-id="859f2-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="859f2-114">L’objet de progression doit utiliser les valeurs des paramètres _ulCount_ et _ulTotal_ de la méthode [IMAPIProgress::P rogress,](imapiprogress-progress.md) qui indiquent respectivement l’élément actuel et le nombre total d’éléments de l’opération, pour incrémenter l’indicateur de progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="859f2-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="859f2-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="859f2-115">_lppProgress_</span></span>
  
> <span data-ttu-id="859f2-116">[out] Pointeur vers un pointeur vers l’objet de progression.</span><span class="sxs-lookup"><span data-stu-id="859f2-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="859f2-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="859f2-117">Return value</span></span>

<span data-ttu-id="859f2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="859f2-118">S_OK</span></span> 
  
> <span data-ttu-id="859f2-119">L’objet de progression a été récupéré avec succès.</span><span class="sxs-lookup"><span data-stu-id="859f2-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="859f2-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="859f2-120">Remarks</span></span>

<span data-ttu-id="859f2-121">La **méthode IMAPISupport::D oProgressDialog** est implémentée pour les objets de prise en charge du carnet d’adresses et du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="859f2-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="859f2-122">Ces fournisseurs **appellent DoProgressDialog** pour accéder à l’implémentation MAPI de l’interface [IMAPIProgress,](imapiprogressiunknown.md) qui calcule les informations de progression et affiche une boîte de dialogue standard.</span><span class="sxs-lookup"><span data-stu-id="859f2-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="859f2-123">Pour plus d’informations sur l’utilisation d’un objet de progression et de l’interface **IMAPIProgress,** voir [Afficher un indicateur de progression.](how-to-display-a-progress-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="859f2-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="859f2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="859f2-124">See also</span></span>



[<span data-ttu-id="859f2-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="859f2-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="859f2-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="859f2-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="859f2-127">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="859f2-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="859f2-128">Affichage d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="859f2-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

