---
title: Sélection d’un dossier de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 87f8b4f4011e405d9848f12b5cae56f27fff1ab8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787091"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="45cfd-103">Sélection d’un dossier de réception</span><span class="sxs-lookup"><span data-stu-id="45cfd-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="45cfd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45cfd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45cfd-105">Un dossier de réception est l’emplacement des messages entrants d’une classe particulière.</span><span class="sxs-lookup"><span data-stu-id="45cfd-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="45cfd-106">Pour IPM et les messages d’état connexes, MAPI affecte la boîte de réception comme le dossier de réception par défaut.</span><span class="sxs-lookup"><span data-stu-id="45cfd-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="45cfd-107">Pour IPC et les messages d’état connexes, MAPI attribue le dossier racine de la banque de messages comme dossier de réception par défaut.</span><span class="sxs-lookup"><span data-stu-id="45cfd-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="45cfd-108">Vous pouvez modifier ces affectations ou effectuer des affectations supplémentaires pour d’autres classes de message.</span><span class="sxs-lookup"><span data-stu-id="45cfd-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="45cfd-109">Émission explicites recevoir des affectations de dossiers pour votre client pris en charge par message classes est facultative.</span><span class="sxs-lookup"><span data-stu-id="45cfd-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="45cfd-110">Lorsqu’une classe de message entrant n’a pas d’un dossier de réception affecté, le fournisseur de banque de messages utilise automatiquement le dossier de réception pour la classe qui correspond à la plus long préfixe possible de la classe entrant.</span><span class="sxs-lookup"><span data-stu-id="45cfd-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="45cfd-111">Par exemple, si votre client reçoit un message de la classe IPM. Recevoir des Note.MyDocument et le seul dossier qui a été établie est la boîte de réception des messages IPM, ce message est placé dans la boîte de réception car IPM. Note.MyDocument dérive de la classe de base IPM.</span><span class="sxs-lookup"><span data-stu-id="45cfd-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="45cfd-112">Lorsque vous affectez un dossier de réception des messages IPC, jamais utiliser un dossier à partir de la sous-arborescence IPM.</span><span class="sxs-lookup"><span data-stu-id="45cfd-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="45cfd-113">Ces dossiers doivent être réservés pour que les messages IPM.</span><span class="sxs-lookup"><span data-stu-id="45cfd-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="45cfd-114">Utilisez plutôt un dossier qui se trouve dans le dossier racine de la banque messages.</span><span class="sxs-lookup"><span data-stu-id="45cfd-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="45cfd-115">**Pour créer un dossier de réception pour une classe de message IPM**</span><span class="sxs-lookup"><span data-stu-id="45cfd-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="45cfd-116">Appeler la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages pour récupérer la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="45cfd-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="45cfd-117">Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) avec **PR_IPM_SUBTREE_ENTRYID** en tant que l’identificateur d’entrée pour ouvrir le dossier racine de la sous-arborescence IPM dans la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="45cfd-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="45cfd-118">Appelez [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) pour créer le dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="45cfd-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="45cfd-119">Appelez [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) pour mapper le nouveau dossier à votre classe de message IPM.</span><span class="sxs-lookup"><span data-stu-id="45cfd-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="45cfd-120">**Pour créer un dossier de réception pour une classe de message IPC**</span><span class="sxs-lookup"><span data-stu-id="45cfd-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="45cfd-121">Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) avec un identificateur d’entrée null pour ouvrir le dossier racine de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="45cfd-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="45cfd-122">Appelez [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) pour créer le dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="45cfd-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="45cfd-123">Appelez [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) pour mapper le nouveau dossier à votre classe de message IPC.</span><span class="sxs-lookup"><span data-stu-id="45cfd-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="45cfd-124">Affecter le dossier de réception que vous utilisez pour les messages pour les messages d’état connexes.</span><span class="sxs-lookup"><span data-stu-id="45cfd-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="45cfd-125">Par exemple, si votre client reçoit IPM. Remarques, définir un dossier de réception pour futur IPM. Remarques et le même dossier des futurs messages Report.IPM.Note de réception.</span><span class="sxs-lookup"><span data-stu-id="45cfd-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

