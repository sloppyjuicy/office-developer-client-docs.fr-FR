---
title: Banques de messages par d�faut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cece19329460b382be724faa9f0f522831cc197c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783117"
---
# <a name="default-message-stores"></a><span data-ttu-id="de4f1-103">Banques de messages par d�faut</span><span class="sxs-lookup"><span data-stu-id="de4f1-103">Default Message Stores</span></span>

  
  
<span data-ttu-id="de4f1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de4f1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de4f1-p101">Une banque de messages par d�faut est celle dont les applications clientes peuvent utiliser pour les t�ches de messagerie � usage g�n�ral. Il existe un certain nombre de fonctionnalit�s facultatives pour les fournisseurs de banque de message qui deviennent obligatoires si le fournisseur de banque de messages doit �tre utilis� en tant que la banque de messages par d�faut. Ils sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="de4f1-p101">A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:</span></span>
  
- <span data-ttu-id="de4f1-108">Impl�mentation de dossiers sp�ciaux : les dossiers bo�te de r�ception, bo�te d'envoi et r�sultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="de4f1-108">Implementing the special folders: the Inbox, Outbox, and search-results folders.</span></span>
    
- <span data-ttu-id="de4f1-109">Fournir des rapports de lecture et nonread.</span><span class="sxs-lookup"><span data-stu-id="de4f1-109">Providing read and nonread reports.</span></span>
    
- <span data-ttu-id="de4f1-110">Autoriser les envois de messages entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="de4f1-110">Allowing incoming and outgoing message submissions.</span></span>
    
- <span data-ttu-id="de4f1-111">Autoriser la cr�ation de messages avec des classes de message arbitraires.</span><span class="sxs-lookup"><span data-stu-id="de4f1-111">Allowing the creation of messages with arbitrary message classes.</span></span>
    
- <span data-ttu-id="de4f1-112">Prise en charge des propri�t�s nomm�es et plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="de4f1-112">Supporting named and multiple-value properties.</span></span>
    
- <span data-ttu-id="de4f1-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span><span class="sxs-lookup"><span data-stu-id="de4f1-113">Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider.</span></span> 
    
- <span data-ttu-id="de4f1-p102">Supporting associated contents tables. For more information, see [Tables des mati�res](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="de4f1-p102">Supporting associated contents tables. For more information, see [Contents Tables](contents-tables.md).</span></span>
    
- <span data-ttu-id="de4f1-116">Prise en charge des notifications de spouleur MAPI lorsqu'il existe des messages dans la file d'attente de messages sortants.</span><span class="sxs-lookup"><span data-stu-id="de4f1-116">Supporting notification of the MAPI spooler when there are messages in the outgoing message queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de4f1-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de4f1-117">See also</span></span>



[<span data-ttu-id="de4f1-118">D�veloppement d'un fournisseur de banque de messages MAPI</span><span class="sxs-lookup"><span data-stu-id="de4f1-118">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

