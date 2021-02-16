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
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329469"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="3cdb1-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="3cdb1-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="3cdb1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cdb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cdb1-105">Annule l’inscription des notifications auprès d’une visionneuse de formulaires précédemment établie en appelant [IMAPIForm::Advise](imapiform-advise.md).</span><span class="sxs-lookup"><span data-stu-id="3cdb1-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="3cdb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cdb1-106">Parameters</span></span>

 <span data-ttu-id="3cdb1-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="3cdb1-107">_ulConnection_</span></span>
  
> <span data-ttu-id="3cdb1-108">[in] Numéro de connexion qui identifie l’inscription de notification à annuler.</span><span class="sxs-lookup"><span data-stu-id="3cdb1-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3cdb1-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3cdb1-109">Return value</span></span>

<span data-ttu-id="3cdb1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3cdb1-110">S_OK</span></span> 
  
> <span data-ttu-id="3cdb1-111">L’inscription a été annulée.</span><span class="sxs-lookup"><span data-stu-id="3cdb1-111">The registration was canceled.</span></span>
    
<span data-ttu-id="3cdb1-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3cdb1-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="3cdb1-113">Le numéro de connexion transmis dans le  _paramètre ulConnection_ ne représente pas une inscription valide.</span><span class="sxs-lookup"><span data-stu-id="3cdb1-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3cdb1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3cdb1-114">Remarks</span></span>

<span data-ttu-id="3cdb1-115">Les visionneuses de formulaires appellent la méthode **IMAPIForm::Unadvise** pour annuler une inscription pour la notification qu’elles ont d’abord établie en appelant la méthode **IMAPIForm::Advise.**</span><span class="sxs-lookup"><span data-stu-id="3cdb1-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3cdb1-116">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="3cdb1-116">Notes to implementers</span></span>

<span data-ttu-id="3cdb1-117">Ignorer le pointeur que vous maintenez dans la vue de la visionneuse de formulaires pour le conseiller en appelant sa méthode [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cdb1-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="3cdb1-118">En règle générale, **Release** est appelé pendant l’appel **Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="3cdb1-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="3cdb1-119">Toutefois, si un autre thread est en train d’appeler l’une des méthodes [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) pour le sink de conseil d’affichage, retardez l’appel release jusqu’à ce que la méthode **IMAPIViewAdviseSink** renvoie. </span><span class="sxs-lookup"><span data-stu-id="3cdb1-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3cdb1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cdb1-120">See also</span></span>



[<span data-ttu-id="3cdb1-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="3cdb1-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="3cdb1-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3cdb1-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="3cdb1-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3cdb1-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

