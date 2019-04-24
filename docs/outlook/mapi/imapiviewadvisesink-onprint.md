---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328783"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="d1739-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="d1739-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="d1739-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1739-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1739-105">Avertit la visionneuse de formulaires de l'état d'impression d'un formulaire.</span><span class="sxs-lookup"><span data-stu-id="d1739-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="d1739-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1739-106">Parameters</span></span>

 <span data-ttu-id="d1739-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="d1739-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="d1739-108">dans Numéro de la dernière page imprimée.</span><span class="sxs-lookup"><span data-stu-id="d1739-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="d1739-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="d1739-109">_hrStatus_</span></span>
  
> <span data-ttu-id="d1739-110">dans Valeur HRESULT indiquant l'état du travail d'impression.</span><span class="sxs-lookup"><span data-stu-id="d1739-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="d1739-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1739-111">Possible values are:</span></span>
    
<span data-ttu-id="d1739-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="d1739-112">S_FALSE</span></span> 
  
> <span data-ttu-id="d1739-113">La tâche d'impression s'est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="d1739-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="d1739-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1739-114">S_OK</span></span> 
  
> <span data-ttu-id="d1739-115">La tâche d'impression est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="d1739-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="d1739-116">Echec</span><span class="sxs-lookup"><span data-stu-id="d1739-116">FAILED</span></span> 
  
> <span data-ttu-id="d1739-117">Le travail d'impression a été terminé en raison d'un échec.</span><span class="sxs-lookup"><span data-stu-id="d1739-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d1739-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d1739-118">Return value</span></span>

<span data-ttu-id="d1739-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1739-119">S_OK</span></span> 
  
> <span data-ttu-id="d1739-120">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="d1739-120">The notification succeeded.</span></span>
    
<span data-ttu-id="d1739-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d1739-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d1739-122">L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton Annuler d'une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d1739-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d1739-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1739-123">Remarks</span></span>

<span data-ttu-id="d1739-124">Les objets de formulaire appellent la méthode **IMAPIViewAdviseSink:: OnPrint** lors de l'impression pour informer la visionneuse de la progression de l'impression.</span><span class="sxs-lookup"><span data-stu-id="d1739-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d1739-125">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="d1739-125">Notes to callers</span></span>

<span data-ttu-id="d1739-126">Si la tâche d'impression implique plusieurs pages, vous pouvez appeler **OnPrint** une fois que chaque page est imprimée.</span><span class="sxs-lookup"><span data-stu-id="d1739-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="d1739-127">Définissez _dwPageNumber_ sur la page actuellement imprimée et _hrStatus_ à S_OK.</span><span class="sxs-lookup"><span data-stu-id="d1739-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="d1739-128">Une fois le travail d'impression terminé, appelez **OnPrint** avec _dwPageNumber_ défini sur la dernière page imprimée et _hrStatus_ définie sur S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="d1739-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="d1739-129">Pour plus d'informations sur les notifications de formulaire, consultez la rubrique [envoi et réception de notifications de formulaire](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="d1739-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d1739-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1739-130">See also</span></span>



[<span data-ttu-id="d1739-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d1739-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

