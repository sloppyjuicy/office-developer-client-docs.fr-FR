---
title: Modèle d’envoi de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8cb34360f5a0a3e67aca1ac53fe639724135f594
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584540"
---
# <a name="message-submission-model"></a><span data-ttu-id="7f8ad-103">Modèle d’envoi de message</span><span class="sxs-lookup"><span data-stu-id="7f8ad-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="7f8ad-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f8ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f8ad-105">Envoi du message est effectuée par une série d’appels du spouleur MAPI vers le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="7f8ad-106">Les appels sont classés comme suit :</span><span class="sxs-lookup"><span data-stu-id="7f8ad-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="7f8ad-107">Le spouleur MAPI appelle [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), en passant un [IMessage : IMAPIProp](imessageimapiprop.md) instance, pour lancer le processus.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="7f8ad-108">Le fournisseur de transport place ensuite une valeur de référence : un transport définies par l’identificateur utilisé dans les futures références à ce message, à l’emplacement référencé dans **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="7f8ad-109">Le fournisseur de transport accède aux données message à l’aide de l’instance **IMessage** passée.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="7f8ad-110">Pour chaque destinataire dans passé **IMessage** pour laquelle il accepte la responsabilité, le fournisseur de transport définit la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) et renvoie.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="7f8ad-111">Le fournisseur de transport peut utiliser la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour indiquer si elle reconnaît tous les destinataires qui ne peuvent pas être remis à, ou pour créer un rapport de remise standard.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="7f8ad-112">**StatusRecips** est pratique pour les fournisseurs de transport que vous avez déterminé que certains destinataires ne peuvent pas être remis à ou qui ont reçu les informations de remise à partir de leur système de messagerie sous-jacent qui peut l’utilisateur ou l’application cliente utiles.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="7f8ad-113">Appel de spouleur MAPI [IXPLogon::EndMessage](ixplogon-endmessage.md) est la main finale responsabilité désactivé pour le message du spouleur MAPI pour le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="7f8ad-114">Le spouleur MAPI permet [IXPLogon::TransportNotify](ixplogon-transportnotify.md) pour annuler pendant les appels **SubmitMessage** ou **EndMessage** de traitement du message.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

