---
title: Navigation dans le dossier de boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5e93dbed0fe56ada5fc41c3e2e51aa3d0c3bef6d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594487"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="9661e-103">Navigation dans le dossier de boîte de réception</span><span class="sxs-lookup"><span data-stu-id="9661e-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="9661e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9661e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9661e-105">**Pour passer en revue tous les messages dans la boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="9661e-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="9661e-106">Appelez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer l’identificateur d’entrée de la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="9661e-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="9661e-107">Appelez **IMAPIFolder::OpenEntry** pour ouvrir la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="9661e-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="9661e-108">Appelez la méthode de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) de la boîte de réception pour récupérer la table des matières.</span><span class="sxs-lookup"><span data-stu-id="9661e-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="9661e-109">Appelez le contenu [IMAPITable::SetColumns](imapitable-setcolumns.md) méthode table pour limiter la colonne valeur **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et les autres colonnes que vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="9661e-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="9661e-110">Appelez [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer un groupe de lignes.</span><span class="sxs-lookup"><span data-stu-id="9661e-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="9661e-111">Jusqu'à ce qu’il ne sont plus toutes les lignes de la table des matières :</span><span class="sxs-lookup"><span data-stu-id="9661e-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="9661e-112">Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir le message représenté par l’identificateur d’entrée de chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="9661e-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="9661e-113">Affecter le paramètre _lppUnk_ à un pointeur d’interface **IMessage** local.</span><span class="sxs-lookup"><span data-stu-id="9661e-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="9661e-114">Utiliser les propriétés du message.</span><span class="sxs-lookup"><span data-stu-id="9661e-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="9661e-115">Libérer le pointeur vers laquelle pointé le paramètre _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="9661e-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="9661e-116">Appelez [IMAPITable::QueryRows](imapitable-queryrows.md) pour extraire le groupe de lignes suivant.</span><span class="sxs-lookup"><span data-stu-id="9661e-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="9661e-117">Version de la table des matières.</span><span class="sxs-lookup"><span data-stu-id="9661e-117">Release the contents table.</span></span>
    

