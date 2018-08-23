---
title: Tables de dossiers de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b88545ede6275bd834fad5869d972e2860a6c77e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573179"
---
# <a name="receive-folder-tables"></a><span data-ttu-id="31c14-103">Tables de dossiers de réception</span><span class="sxs-lookup"><span data-stu-id="31c14-103">Receive Folder Tables</span></span>

  
  
<span data-ttu-id="31c14-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31c14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31c14-105">Une table de dossier de réception contient des informations pour tous les dossiers désignés en tant que dossiers de réception pour une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="31c14-105">A receive folder table contains information for all the folders designated as receive folders for a message store.</span></span> <span data-ttu-id="31c14-106">Un dossier de réception est un dossier où les messages entrants d’une classe de message particulier sont placés.</span><span class="sxs-lookup"><span data-stu-id="31c14-106">A receive folder is a folder where incoming messages of a particular message class are placed.</span></span> <span data-ttu-id="31c14-107">Message d’implémentés par les fournisseurs de banque de recevoir des tables du dossier et applications clientes les utilisent en effectuant un appel à la méthode [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="31c14-107">Message store providers implement receive folder tables and client applications use them by making a call to the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="31c14-108">Le suivant propriétés constituent la colonne obligatoire recevoir des tables de dossier :</span><span class="sxs-lookup"><span data-stu-id="31c14-108">The following properties make up the required column set in receive folder tables:</span></span>
  
 <span data-ttu-id="31c14-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="31c14-109">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="31c14-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="31c14-110">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span> 
  
 <span data-ttu-id="31c14-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="31c14-111">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="31c14-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31c14-112">See also</span></span>



[<span data-ttu-id="31c14-113">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="31c14-113">MAPI Tables</span></span>](mapi-tables.md)

