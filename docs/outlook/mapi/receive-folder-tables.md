---
title: Tables de dossiers de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328475"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="0284e-103">Tables de dossiers de réception</span><span class="sxs-lookup"><span data-stu-id="0284e-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="0284e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0284e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0284e-105">Une table de dossiers de réception contient des informations pour tous les dossiers désignés comme dossiers de réception pour une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="0284e-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="0284e-106">Un dossier de réception est un dossier où les messages entrants d'une classe de message particulière sont placés.</span><span class="sxs-lookup"><span data-stu-id="0284e-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="0284e-107">Les fournisseurs de banque de messages implémentent les tables de dossiers de réception et les applications clientes les utilisent en appelant la méthode [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="0284e-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="0284e-108">Les propriétés suivantes constituent le jeu de colonnes requis dans les tables de dossiers de réception:</span><span class="sxs-lookup"><span data-stu-id="0284e-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="0284e-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0284e-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="0284e-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0284e-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="0284e-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="0284e-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0284e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0284e-112">See also</span></span>



[<span data-ttu-id="0284e-113">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="0284e-113">MAPI Tables</span></span>](mapi-tables.md)

