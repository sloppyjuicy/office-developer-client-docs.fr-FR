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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286982"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="8f05b-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="8f05b-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="8f05b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f05b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f05b-105">Annule une inscription aux notifications précédemment établie pour une entrée de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="8f05b-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="8f05b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f05b-106">Parameters</span></span>

 <span data-ttu-id="8f05b-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="8f05b-107">_ulConnection_</span></span>
  
> <span data-ttu-id="8f05b-108">dans Numéro de connexion qui représente l'inscription à annuler.</span><span class="sxs-lookup"><span data-stu-id="8f05b-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="8f05b-109">Le paramètre _ulConnection_ doit contenir une valeur renvoyée par un appel antérieur à la méthode [IAddrBook:: Advise](iaddrbook-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="8f05b-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8f05b-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8f05b-110">Return value</span></span>

<span data-ttu-id="8f05b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f05b-111">S_OK</span></span> 
  
> <span data-ttu-id="8f05b-112">L'inscription a été annulée.</span><span class="sxs-lookup"><span data-stu-id="8f05b-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8f05b-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="8f05b-113">Remarks</span></span>

<span data-ttu-id="8f05b-114">Les clients appellent \*\*\*\* la méthode Unadvise pour cesser de recevoir des notifications sur les modifications apportées à une entrée de carnet d'adresses particulière.</span><span class="sxs-lookup"><span data-stu-id="8f05b-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="8f05b-115">Lorsqu'une inscription aux notifications est annulée, le fournisseur de carnet d'adresses libère son pointeur vers le récepteur de notifications de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="8f05b-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="8f05b-116">Toutefois, la publication peut se produire pendant \*\*\*\* l'appel Unadvise ou ultérieurement, si un autre thread appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="8f05b-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="8f05b-117">Lorsqu'une notification est en cours, la publication est retardée jusqu'à ce que la méthode **OnNotify** renvoie.</span><span class="sxs-lookup"><span data-stu-id="8f05b-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f05b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f05b-118">See also</span></span>



[<span data-ttu-id="8f05b-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="8f05b-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="8f05b-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="8f05b-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="8f05b-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8f05b-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

