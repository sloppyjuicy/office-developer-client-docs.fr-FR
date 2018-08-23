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
ms.openlocfilehash: 32174e213334d784220b960364443e60db6d1d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582776"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="d2a5b-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="d2a5b-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="d2a5b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2a5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2a5b-105">Récupère un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="d2a5b-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="d2a5b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2a5b-106">Parameters</span></span>

 <span data-ttu-id="d2a5b-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d2a5b-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d2a5b-108">[in] Un handle vers la fenêtre parent de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="d2a5b-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="d2a5b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d2a5b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d2a5b-110">[in] Masque de bits d’indicateurs qui contrôle comment l’objet de l’avancement doit calculer l’avancement.</span><span class="sxs-lookup"><span data-stu-id="d2a5b-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="d2a5b-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="d2a5b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d2a5b-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="d2a5b-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="d2a5b-113">Progression est calculée pour un élément de niveau supérieur, par exemple un dossier parent.</span><span class="sxs-lookup"><span data-stu-id="d2a5b-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="d2a5b-114">L’objet de l’avancement doit utiliser les valeurs dans la méthode [IMAPIProgress::Progress](imapiprogress-progress.md) _ulCount_ et _ulTotal_ — qui indiquent l’élément actuel et le nombre total d’éléments dans l’opération, respectivement, pour incrémenter la progression indicateur de l’opération.</span><span class="sxs-lookup"><span data-stu-id="d2a5b-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="d2a5b-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="d2a5b-115">_lppProgress_</span></span>
  
> <span data-ttu-id="d2a5b-116">[out] Pointeur vers un pointeur vers l’objet de progression.</span><span class="sxs-lookup"><span data-stu-id="d2a5b-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d2a5b-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d2a5b-117">Return value</span></span>

<span data-ttu-id="d2a5b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2a5b-118">S_OK</span></span> 
  
> <span data-ttu-id="d2a5b-119">La progression de l’objet a été extrait.</span><span class="sxs-lookup"><span data-stu-id="d2a5b-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2a5b-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2a5b-120">Remarks</span></span>

<span data-ttu-id="d2a5b-121">La méthode **IMAPISupport::DoProgressDialog** est implémentée pour adresse livre et message fournisseur prise en charge des objets store.</span><span class="sxs-lookup"><span data-stu-id="d2a5b-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="d2a5b-122">Ces fournisseurs appellent **DoProgressDialog** pour accéder à l’implémentation de l’interface [IMAPIProgress](imapiprogressiunknown.md) , qui calcule les informations de progression et affiche une boîte de dialogue standard MAPI.</span><span class="sxs-lookup"><span data-stu-id="d2a5b-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="d2a5b-123">Pour plus d’informations sur l’utilisation d’un objet de progression et l’interface **IMAPIProgress** , voir [Afficher un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="d2a5b-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d2a5b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2a5b-124">See also</span></span>



[<span data-ttu-id="d2a5b-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2a5b-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="d2a5b-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="d2a5b-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="d2a5b-127">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2a5b-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="d2a5b-128">Afficher un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="d2a5b-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

