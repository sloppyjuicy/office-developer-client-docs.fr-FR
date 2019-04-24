---
title: Parcours du dossier boîte de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ad1459f-d59a-4784-94ea-4cad194e6e50
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e954cb2d8029a31e7f69daaa7e8ed55a7953ac02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356580"
---
# <a name="traversing-the-inbox-folder"></a><span data-ttu-id="f5d6c-103">Parcours du dossier boîte de réception</span><span class="sxs-lookup"><span data-stu-id="f5d6c-103">Traversing the Inbox Folder</span></span>

  
  
<span data-ttu-id="f5d6c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5d6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="f5d6c-105">**Pour parcourir tous les messages de la boîte de réception**</span><span class="sxs-lookup"><span data-stu-id="f5d6c-105">**To cycle through all of the messages in the Inbox**</span></span>
  
1. <span data-ttu-id="f5d6c-106">Appelez [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) pour récupérer l'identificateur d'entrée de la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-106">Call [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) to retrieve the entry identifier of the Inbox.</span></span> 
    
2. <span data-ttu-id="f5d6c-107">Appelez **IMAPIFolder:: OpenEntry** pour ouvrir la boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-107">Call **IMAPIFolder::OpenEntry** to open the Inbox.</span></span> 
    
3. <span data-ttu-id="f5d6c-108">Appelez la méthode [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) de la boîte de réception pour extraire la table de contenu.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-108">Call the Inbox's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to retrieve the contents table.</span></span> 
    
4. <span data-ttu-id="f5d6c-109">Appelez la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la table contents pour limiter la valeur de la colonne à **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et toutes les autres colonnes requises.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-109">Call the contents table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and any other columns you require.</span></span> 
    
5. <span data-ttu-id="f5d6c-110">Appeler [IMAPITable:: QueryRows](imapitable-queryrows.md) pour récupérer un groupe de lignes.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-110">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve a group of rows.</span></span> 
    
6. <span data-ttu-id="f5d6c-111">Jusqu'à ce qu'il n'y ait plus de lignes dans la table Contents:</span><span class="sxs-lookup"><span data-stu-id="f5d6c-111">Until there are no longer any rows in the contents table:</span></span>
    
1. <span data-ttu-id="f5d6c-112">Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) pour ouvrir le message représenté par l'identificateur d'entrée de chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-112">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) to open the message represented by the entry identifier from each row.</span></span> 
    
2. <span data-ttu-id="f5d6c-113">AsSignez le paramètre _lppUnk_ à un pointeur d'interface **IMessage** local.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-113">Assign the  _lppUnk_ parameter to a local **IMessage** interface pointer.</span></span> 
    
3. <span data-ttu-id="f5d6c-114">Utiliser les propriétés du message.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-114">Work with the properties of the message.</span></span>
    
4. <span data-ttu-id="f5d6c-115">ReLâchez le pointeur pointé par le paramètre _lppUnk_ .</span><span class="sxs-lookup"><span data-stu-id="f5d6c-115">Release the pointer pointed to by the  _lppUnk_ parameter.</span></span> 
    
5. <span data-ttu-id="f5d6c-116">Appelez [IMAPITable:: QueryRows](imapitable-queryrows.md) pour extraire le groupe de lignes suivant.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-116">Call [IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve the next group of rows.</span></span> 
    
7. <span data-ttu-id="f5d6c-117">Libérez la table des matières.</span><span class="sxs-lookup"><span data-stu-id="f5d6c-117">Release the contents table.</span></span>
    

