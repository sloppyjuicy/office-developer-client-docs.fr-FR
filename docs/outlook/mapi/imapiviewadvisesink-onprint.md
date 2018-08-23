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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 202d461d4acefe18e69b47db9319cb328c61406e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592317"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="f363e-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="f363e-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="f363e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f363e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f363e-105">Avertit l’utilisateur du formulaire de l’état d’impression d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="f363e-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="f363e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f363e-106">Parameters</span></span>

 <span data-ttu-id="f363e-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="f363e-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="f363e-108">[in] Numéro de la dernière page imprimée.</span><span class="sxs-lookup"><span data-stu-id="f363e-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="f363e-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="f363e-109">_hrStatus_</span></span>
  
> <span data-ttu-id="f363e-110">[in] Une valeur HRESULT indiquant l’état de l’impression.</span><span class="sxs-lookup"><span data-stu-id="f363e-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="f363e-111">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f363e-111">Possible values are:</span></span>
    
<span data-ttu-id="f363e-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="f363e-112">S_FALSE</span></span> 
  
> <span data-ttu-id="f363e-113">Le travail d’impression est terminée et réussie.</span><span class="sxs-lookup"><span data-stu-id="f363e-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="f363e-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="f363e-114">S_OK</span></span> 
  
> <span data-ttu-id="f363e-115">Le travail d’impression est en cours.</span><span class="sxs-lookup"><span data-stu-id="f363e-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="f363e-116">A ÉCHOUÉ</span><span class="sxs-lookup"><span data-stu-id="f363e-116">FAILED</span></span> 
  
> <span data-ttu-id="f363e-117">Le travail d’impression a été interrompu en raison d’une défaillance.</span><span class="sxs-lookup"><span data-stu-id="f363e-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f363e-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f363e-118">Return value</span></span>

<span data-ttu-id="f363e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f363e-119">S_OK</span></span> 
  
> <span data-ttu-id="f363e-120">La notification a réussi.</span><span class="sxs-lookup"><span data-stu-id="f363e-120">The notification succeeded.</span></span>
    
<span data-ttu-id="f363e-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f363e-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f363e-122">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton d’annulation dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f363e-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f363e-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="f363e-123">Remarks</span></span>

<span data-ttu-id="f363e-124">Objets de formulaire appeler la méthode **IMAPIViewAdviseSink::OnPrint** lors de l’impression pour informer l’Afficheur de progression de l’impression.</span><span class="sxs-lookup"><span data-stu-id="f363e-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f363e-125">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="f363e-125">Notes to callers</span></span>

<span data-ttu-id="f363e-126">Si le travail d’impression implique plusieurs pages, vous pouvez appeler **OnPrint** après que chaque page est imprimé.</span><span class="sxs-lookup"><span data-stu-id="f363e-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="f363e-127">Valeur _dwPageNumber_ à la page en cours d’impression et _hrStatus_ S_OK.</span><span class="sxs-lookup"><span data-stu-id="f363e-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="f363e-128">Lorsque le travail d’impression est terminé, appel **OnPrint** avec _dwPageNumber_ défini à la dernière page imprimée et _hrStatus_ valeur S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="f363e-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="f363e-129">Pour plus d’informations sur les notifications de formulaire, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="f363e-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f363e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f363e-130">See also</span></span>



[<span data-ttu-id="f363e-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f363e-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

