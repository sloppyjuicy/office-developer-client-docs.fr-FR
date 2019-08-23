---
title: Banques de messages par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 1ad325c68241c8a3924909b4dbf42c9657e68352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338044"
---
# <a name="default-message-stores"></a><span data-ttu-id="993f8-103">Banques de messages par défaut</span><span class="sxs-lookup"><span data-stu-id="993f8-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="993f8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="993f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="993f8-p101">Une banque de messages par défaut est une banque de messages pouvant être utilisée par les applications clientes pour des tâches de messagerie à usage général. Certaines fonctionnalités facultatives pour les fournisseurs de banques de messages deviennent nécessaires si le fournisseur de banques de messages doit être utilisé en tant que banque de messages par défaut. Ces fonctionnalités sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="993f8-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="993f8-108">Implémentation des dossiers spéciaux : les dossiers Boîte de réception, Boîte d’envoi et résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="993f8-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="993f8-109">Fournir des rapports de lecture et nonread.</span><span class="sxs-lookup"><span data-stu-id="993f8-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="993f8-110">Autoriser les envois de messages entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="993f8-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="993f8-111">Autorisation de la création de messages avec classes de messages arbitraires.</span><span class="sxs-lookup"><span data-stu-id="993f8-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="993f8-112">Prise en charge des propriétés nommées et à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="993f8-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="993f8-113">Prise en charge de la méthode [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md), même si le fournisseur de banques de messages est étroitement associé à un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="993f8-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="993f8-p102">Prise en charge des tables des matières associées. Pour plus d’informations, reportez-vous à [Tables des matières](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="993f8-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="993f8-116">Prise en charge des notifications de spouleur MAPI lorsqu'il existe des messages dans la file d'attente de messages sortants.</span><span class="sxs-lookup"><span data-stu-id="993f8-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="993f8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="993f8-117">See also</span></span>



[<span data-ttu-id="993f8-118">Développement d’un fournisseur de banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="993f8-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

