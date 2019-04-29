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
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="93eb0-103">Envoi de rapports de remise de messages</span><span class="sxs-lookup"><span data-stu-id="93eb0-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="93eb0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93eb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93eb0-105">Certains systèmes de messagerie sous-jacents prennent en charge les rapports de remise et d'autres non.</span><span class="sxs-lookup"><span data-stu-id="93eb0-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="93eb0-106">La manière dont le fournisseur de transport détermine si les rapports de remise de messages ou de non-remise peuvent être envoyés aux applications clientes est un détail d'implémentation spécifique aux fournisseurs de transport individuels.</span><span class="sxs-lookup"><span data-stu-id="93eb0-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="93eb0-107">Si des rapports de remise peuvent être envoyés aux applications clientes, les fournisseurs de transport utilisent la méthode [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) pour informer MAPI de la réussite ou de l'échec de la remise d'un ou de plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="93eb0-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="93eb0-108">MAPI génère ensuite des rapports de remise ou de livraison correspondant à ces destinataires.</span><span class="sxs-lookup"><span data-stu-id="93eb0-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="93eb0-109">Les fournisseurs de transport peuvent également convertir les rapports de remise et de non remise entrants natifs du système de messagerie en rapports de remise et de non remise MAPI au moyen de **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="93eb0-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

