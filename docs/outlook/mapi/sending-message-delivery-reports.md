---
title: Envoi de rapports de remise de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 717494f30fd4d43e94a7c6a37770e2eab8ebb59e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593598"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="5d243-103">Envoi de rapports de remise de messages</span><span class="sxs-lookup"><span data-stu-id="5d243-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="5d243-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d243-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d243-105">Certains systèmes de messagerie sous-jacent prend en charge les rapports de remise et d’autres pas.</span><span class="sxs-lookup"><span data-stu-id="5d243-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="5d243-106">Comment le fournisseur de transport détermine si les rapports de remise ou de non-remise du message peuvent être envoyés vers des applications clientes est un détail d’implémentation spécifique à un fournisseur de transport individuels.</span><span class="sxs-lookup"><span data-stu-id="5d243-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="5d243-107">Si les rapports de remise peuvent être envoyés vers les applications clientes, fournisseurs de transport utilisent la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour notifier MAPI de remise réussi ou échoué pour un ou plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="5d243-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="5d243-108">MAPI puis génère des rapports de remise ou de non-remise correspondant à des destinataires.</span><span class="sxs-lookup"><span data-stu-id="5d243-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="5d243-109">Fournisseurs de transport peuvent également traduire les rapports de remise et de non-remise entrants natifs au système de messagerie dans remise MAPI et les rapports de non-remise prenait **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="5d243-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

