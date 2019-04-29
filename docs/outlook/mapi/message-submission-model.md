---
title: Modèle de dépôt des messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421122"
---
# <a name="message-submission-model"></a><span data-ttu-id="258cb-103">Modèle de dépôt des messages</span><span class="sxs-lookup"><span data-stu-id="258cb-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="258cb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="258cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="258cb-105">L'envoi de messages est effectué par une série d'appels depuis le spouleur MAPI vers le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="258cb-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="258cb-106">Les appels sont séquencés comme suit:</span><span class="sxs-lookup"><span data-stu-id="258cb-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="258cb-107">Le spouleur MAPI appelle [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md), en transmettant une instance [IMessage: IMAPIProp](imessageimapiprop.md) , pour commencer le processus.</span><span class="sxs-lookup"><span data-stu-id="258cb-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="258cb-108">Le fournisseur de transport place ensuite une valeur de référence, c'est-à-dire un identificateur défini par le transport utilisé dans les références futures à ce message, à l'emplacement référencé dans **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="258cb-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="258cb-109">Le fournisseur de transport accède aux données de message à l'aide de l'instance **IMessage** passée.</span><span class="sxs-lookup"><span data-stu-id="258cb-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="258cb-110">Pour chaque destinataire dans l' **IMessage** passé pour lequel il accepte la responsabilité, le fournisseur de transport définit la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)), puis renvoie.</span><span class="sxs-lookup"><span data-stu-id="258cb-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="258cb-111">Le fournisseur de transport peut utiliser la méthode [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) pour indiquer s'il reconnaît tous les destinataires qui ne peuvent pas être remis à ou pour créer un rapport de remise standard.</span><span class="sxs-lookup"><span data-stu-id="258cb-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="258cb-112">**StatusRecips** est pratique pour les fournisseurs de transport qui ont déterminé que certains des destinataires ne peuvent pas être remis à ou qui ont reçu des informations de remise de la part de leur système de messagerie sous-jacent, que l'utilisateur ou l'application cliente pourrait trouver utile.</span><span class="sxs-lookup"><span data-stu-id="258cb-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="258cb-113">L'appel du spouleur MAPI vers [IXPLogon:: EndMessage](ixplogon-endmessage.md) est la responsabilité finale du message du spouleur MAPI vers le fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="258cb-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="258cb-114">Le spouleur MAPI peut utiliser [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) pour annuler le traitement des messages pendant les appels **SubmitMessage** ou **EndMessage** .</span><span class="sxs-lookup"><span data-stu-id="258cb-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

