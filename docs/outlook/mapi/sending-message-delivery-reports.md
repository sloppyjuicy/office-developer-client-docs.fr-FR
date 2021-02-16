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
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433079"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="dfe03-103">Envoi de rapports de remise de messages</span><span class="sxs-lookup"><span data-stu-id="dfe03-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="dfe03-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfe03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfe03-105">Certains systèmes de messagerie sous-jacents sont en charge des rapports de remise et d’autres non.</span><span class="sxs-lookup"><span data-stu-id="dfe03-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="dfe03-106">La façon dont le fournisseur de transport détermine si des rapports de remise de messages ou de non remise peuvent être envoyés à des applications clientes est un détail d’implémentation propre à des fournisseurs de transport individuels.</span><span class="sxs-lookup"><span data-stu-id="dfe03-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="dfe03-107">Si des rapports de remise peuvent être envoyés à des applications clientes, les fournisseurs de transport utilisent la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour informer MAPI de la réussite ou de l’échec de la remise pour un ou plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="dfe03-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="dfe03-108">MAPI génère ensuite des rapports de remise ou de non remise correspondant à ces destinataires.</span><span class="sxs-lookup"><span data-stu-id="dfe03-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="dfe03-109">Les fournisseurs de transport peuvent également traduire les rapports de remise et de remise entrants natifs du système de messagerie en rapports de remise et de non remise MAPI au moyen de **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="dfe03-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

