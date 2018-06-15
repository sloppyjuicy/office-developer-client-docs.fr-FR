---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: bf72e6f182f67861f909e21f0ec1871d76617974
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19783645"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="bea15-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="bea15-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="bea15-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bea15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bea15-105">Annule l’inscription d’une notification précédemment établie pour une entrée de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="bea15-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="bea15-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bea15-106">Parameters</span></span>

 <span data-ttu-id="bea15-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="bea15-107">_ulConnection_</span></span>
  
> <span data-ttu-id="bea15-108">[in] Un numéro de connexion qui représente l’inscription d’être annulée.</span><span class="sxs-lookup"><span data-stu-id="bea15-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="bea15-109">Le paramètre _ulConnection_ doit contenir une valeur renvoyée par un appel précédent à la méthode [IAddrBook::Advise](iaddrbook-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="bea15-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bea15-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="bea15-110">Return value</span></span>

<span data-ttu-id="bea15-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bea15-111">S_OK</span></span> 
  
> <span data-ttu-id="bea15-112">L’enregistrement a été annulée.</span><span class="sxs-lookup"><span data-stu-id="bea15-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bea15-113">Note</span><span class="sxs-lookup"><span data-stu-id="bea15-113">Remarks</span></span>

<span data-ttu-id="bea15-114">Clients appellent la méthode **Unadvise** pour arrêter de recevoir des notifications sur les modifications apportées à une entrée de carnet d’adresses particulière.</span><span class="sxs-lookup"><span data-stu-id="bea15-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="bea15-115">Lorsqu’un enregistrement de notification est annulé, le carnet d’adresses versions fournisseur son pointeur vers l’appelant de notification récepteur.</span><span class="sxs-lookup"><span data-stu-id="bea15-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="bea15-116">Toutefois, la version peut se produire lors de l’appel **Unadvise** ou ultérieurement, si un autre thread est en appelant la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="bea15-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="bea15-117">Lorsqu’une notification est en cours, la version est différée jusqu'à ce que la méthode **OnNotify** renvoie.</span><span class="sxs-lookup"><span data-stu-id="bea15-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bea15-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bea15-118">See also</span></span>



[<span data-ttu-id="bea15-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="bea15-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="bea15-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="bea15-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="bea15-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bea15-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

