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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285205"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="b2028-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="b2028-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="b2028-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2028-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2028-105">Récupère un objet de progression qui affiche un indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="b2028-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="b2028-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2028-106">Parameters</span></span>

 <span data-ttu-id="b2028-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b2028-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b2028-108">dans Handle de la fenêtre parent de l'indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="b2028-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="b2028-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2028-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b2028-110">dans Masque de des indicateurs qui contrôle la manière dont l'objet Progress doit calculer la progression.</span><span class="sxs-lookup"><span data-stu-id="b2028-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="b2028-111">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="b2028-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b2028-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="b2028-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="b2028-113">La progression est calculée pour un élément de niveau supérieur, tel qu'un dossier parent.</span><span class="sxs-lookup"><span data-stu-id="b2028-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="b2028-114">L'objet Progress doit utiliser les valeurs des paramètres _ulCount_ et _ulTotal_ de la méthode [méthode imapiprogress::P rogress](imapiprogress-progress.md) , qui indiquent respectivement l'élément actif et le nombre total d'éléments dans l'opération; pour incrémenter la progression indicateur de l'opération.</span><span class="sxs-lookup"><span data-stu-id="b2028-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="b2028-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="b2028-115">_lppProgress_</span></span>
  
> <span data-ttu-id="b2028-116">remarquer Pointeur vers un pointeur vers l'objet de progression.</span><span class="sxs-lookup"><span data-stu-id="b2028-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b2028-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b2028-117">Return value</span></span>

<span data-ttu-id="b2028-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2028-118">S_OK</span></span> 
  
> <span data-ttu-id="b2028-119">L'objet Progress a été correctement récupéré.</span><span class="sxs-lookup"><span data-stu-id="b2028-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b2028-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="b2028-120">Remarks</span></span>

<span data-ttu-id="b2028-121">La méthode **IMAPISupport::D oprogressdialog** est implémentée pour les objets de prise en charge des fournisseurs de banques de messages et de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="b2028-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="b2028-122">Ces fournisseurs appellent **DoProgressDialog** pour accéder à l'implémentation MAPI de l'interface [méthode imapiprogress](imapiprogressiunknown.md) , qui calcule les informations d'avancement et affiche une boîte de dialogue standard.</span><span class="sxs-lookup"><span data-stu-id="b2028-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="b2028-123">Pour plus d'informations sur l'utilisation d'un objet Progress et de l'interface **méthode imapiprogress** , voir [afficher un indicateur de progression](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="b2028-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2028-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2028-124">See also</span></span>



[<span data-ttu-id="b2028-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2028-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="b2028-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="b2028-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="b2028-127">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2028-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="b2028-128">Affichage d’un indicateur de progression</span><span class="sxs-lookup"><span data-stu-id="b2028-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

