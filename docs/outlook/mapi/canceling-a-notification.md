---
title: Annulation d’une Notification
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 8cd96dd22daeb98646a62672bd17f7de4d2f7dab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783002"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="d5ec1-103">Annulation d’une Notification</span><span class="sxs-lookup"><span data-stu-id="d5ec1-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="d5ec1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5ec1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5ec1-105">Pour annuler une notification, les clients appellent **Unadvise** méthode d’une source advise.</span><span class="sxs-lookup"><span data-stu-id="d5ec1-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="d5ec1-106">L’appel de **Unadvise** est important car le fournisseur de services libérer la référence à votre récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="d5ec1-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="d5ec1-107">Dans la mesure où un fournisseur de services gère une référence à un récepteur de notifications, le récepteur de notifications peut continuer à recevoir des appels [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ec1-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="d5ec1-108">En fait, en raison de la nature de notification d’événement asynchrone, les clients peuvent être avertis même après une réussite **Unadvise** appeler.</span><span class="sxs-lookup"><span data-stu-id="d5ec1-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="d5ec1-109">Clients doivent être en mesure de gérer la réception des notifications à tout moment.</span><span class="sxs-lookup"><span data-stu-id="d5ec1-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="d5ec1-110">Comme les implémentations de fournisseur de service sont différents, les clients qui ont échoué pour appeler **Unadvise** pour annuler une notification ne peut pas supposez rien sur lorsqu’un fournisseur libère sa référence à leur récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="d5ec1-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="d5ec1-111">Certains fournisseurs de services libérer leurs références pour les récepteurs de notifications lorsque libèrent leurs sources advise.</span><span class="sxs-lookup"><span data-stu-id="d5ec1-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="d5ec1-112">Certains fournisseurs de services ne mais pas.</span><span class="sxs-lookup"><span data-stu-id="d5ec1-112">Some service providers do not.</span></span> <span data-ttu-id="d5ec1-113">Dans la mesure où un fournisseur de services gère une référence à un récepteur de notifications, ce récepteur de notifications peut continuer à recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="d5ec1-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

