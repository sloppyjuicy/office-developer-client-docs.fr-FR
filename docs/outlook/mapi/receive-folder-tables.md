---
title: Tables des dossiers de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417349"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="c5634-103">Tables des dossiers de réception</span><span class="sxs-lookup"><span data-stu-id="c5634-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="c5634-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5634-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5634-105">Une table de dossiers de réception contient des informations pour tous les dossiers désignés comme dossiers de réception pour une magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="c5634-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="c5634-106">Un dossier de réception est un dossier dans lequel les messages entrants d’une classe de message particulière sont placés.</span><span class="sxs-lookup"><span data-stu-id="c5634-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="c5634-107">Les fournisseurs de magasins de messages implémentent les tables de dossiers de réception et les applications clientes les utilisent en appelant la méthode [IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="c5634-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="c5634-108">Les propriétés suivantes définissent le jeu de colonnes requis dans les tables des dossiers de réception :</span><span class="sxs-lookup"><span data-stu-id="c5634-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="c5634-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c5634-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="c5634-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c5634-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="c5634-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c5634-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c5634-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5634-112">See also</span></span>



[<span data-ttu-id="c5634-113">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="c5634-113">MAPI Tables</span></span>](mapi-tables.md)

