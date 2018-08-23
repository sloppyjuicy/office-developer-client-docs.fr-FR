---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 33287d8ac6b1faeba8b8746a95850f6fd1c37462
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579486"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="a62c7-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="a62c7-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="a62c7-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a62c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a62c7-105">Annule une inscription pour les notifications avec une visionneuse de formulaire précédemment établie en appelant [IMAPIForm::Advise](imapiform-advise.md).</span><span class="sxs-lookup"><span data-stu-id="a62c7-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="a62c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a62c7-106">Parameters</span></span>

 <span data-ttu-id="a62c7-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="a62c7-107">_ulConnection_</span></span>
  
> <span data-ttu-id="a62c7-108">[in] Un numéro de connexion qui identifie l’enregistrement de notification d’être annulée.</span><span class="sxs-lookup"><span data-stu-id="a62c7-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a62c7-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a62c7-109">Return value</span></span>

<span data-ttu-id="a62c7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a62c7-110">S_OK</span></span> 
  
> <span data-ttu-id="a62c7-111">L’enregistrement a été annulée.</span><span class="sxs-lookup"><span data-stu-id="a62c7-111">The registration was canceled.</span></span>
    
<span data-ttu-id="a62c7-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a62c7-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="a62c7-113">Le numéro de connexion passé dans le paramètre _ulConnection_ ne représente pas un enregistrement valid.</span><span class="sxs-lookup"><span data-stu-id="a62c7-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a62c7-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a62c7-114">Remarks</span></span>

<span data-ttu-id="a62c7-115">Visionneuses de formulaire appeler la méthode **IMAPIForm::Unadvise** pour annuler une inscription pour la notification qui ils tout d’abord établies en appelant la méthode **IMAPIForm::Advise** .</span><span class="sxs-lookup"><span data-stu-id="a62c7-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a62c7-116">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="a62c7-116">Notes to implementers</span></span>

<span data-ttu-id="a62c7-117">Ignorer le pointeur qui vous sont maintenant à l’affichage de l’utilisateur du formulaire de notification récepteur en appelant la méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a62c7-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="a62c7-118">En règle générale, la **version** est appelé pendant l’appel **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="a62c7-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="a62c7-119">Toutefois, si un autre thread est en appelant une des méthodes [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) pour l’affichage de notification récepteur, différer l’appel de la **version** jusqu'à ce que la méthode **IMAPIViewAdviseSink** renvoie.</span><span class="sxs-lookup"><span data-stu-id="a62c7-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a62c7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a62c7-120">See also</span></span>



[<span data-ttu-id="a62c7-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="a62c7-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="a62c7-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a62c7-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="a62c7-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a62c7-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

