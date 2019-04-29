---
title: Annulation d'une notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409761"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="03bf9-103">Annulation d'une notification</span><span class="sxs-lookup"><span data-stu-id="03bf9-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="03bf9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03bf9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03bf9-105">Pour annuler une notification, les clients appellent la méthode Unadvise de la source de notification. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="03bf9-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="03bf9-106">L' \*\*\*\* appel de Unadvise est important, car il permet au fournisseur de services de libérer sa référence à votre récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="03bf9-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="03bf9-107">Tant qu'un fournisseur de services gère une référence à un récepteur de notification, le récepteur de notifications peut continuer à recevoir des appels [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="03bf9-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="03bf9-108">En fait, en raison de la nature asynchrone de la notification d'événement, les clients peuvent être avertis \*\*\*\* même après un appel Unadvise réussi.</span><span class="sxs-lookup"><span data-stu-id="03bf9-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="03bf9-109">Les clients doivent être en mesure de gérer la réception des notifications à tout moment.</span><span class="sxs-lookup"><span data-stu-id="03bf9-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="03bf9-110">Étant donné que les implémentations de fournisseur de services diffèrent \*\*\*\* , les clients qui ne peuvent pas appeler Unadvise pour annuler une notification ne peuvent pas supposer que le fournisseur libère sa référence à son récepteur de notification.</span><span class="sxs-lookup"><span data-stu-id="03bf9-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="03bf9-111">Certains fournisseurs de services libèrent leurs références aux récepteurs de notification lorsqu'ils libèrent leurs sources de notification.</span><span class="sxs-lookup"><span data-stu-id="03bf9-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="03bf9-112">Certains fournisseurs de services ne le font pas.</span><span class="sxs-lookup"><span data-stu-id="03bf9-112">Some service providers do not.</span></span> <span data-ttu-id="03bf9-113">Tant qu'un fournisseur de services gère une référence à un récepteur de notification, ce récepteur peut continuer à recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="03bf9-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

