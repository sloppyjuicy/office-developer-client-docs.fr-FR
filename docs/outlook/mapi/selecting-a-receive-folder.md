---
title: Sélection d'un dossier de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428416"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="8eeab-103">Sélection d'un dossier de réception</span><span class="sxs-lookup"><span data-stu-id="8eeab-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="8eeab-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8eeab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8eeab-105">Un dossier de réception désigne l'emplacement où les messages entrants d'une classe particulière sont placés.</span><span class="sxs-lookup"><span data-stu-id="8eeab-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="8eeab-106">Pour les messages IPM et related Report, MAPI affecte la boîte de réception en tant que dossier de réception par défaut.</span><span class="sxs-lookup"><span data-stu-id="8eeab-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="8eeab-107">Pour les messages IPC et les rapports connexes, MAPI affecte le dossier racine de la Banque de messages comme dossier de réception par défaut.</span><span class="sxs-lookup"><span data-stu-id="8eeab-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="8eeab-108">Vous pouvez modifier ces affectations ou créer des affectations supplémentaires pour d'autres classes de message.</span><span class="sxs-lookup"><span data-stu-id="8eeab-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="8eeab-109">La création d'attributions de dossiers de réception explicites pour les classes de message prises en charge par votre client est facultative.</span><span class="sxs-lookup"><span data-stu-id="8eeab-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="8eeab-110">Lorsqu'une classe de message entrant ne dispose pas d'un dossier de réception affecté, le fournisseur de banque de messages utilise automatiquement le dossier de réception de la classe qui correspond au plus long préfixe de la classe entrante.</span><span class="sxs-lookup"><span data-stu-id="8eeab-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="8eeab-111">Par exemple, si votre client reçoit un message de la classe IPM. Note. MyDocument et le seul dossier de réception qui a été établi est la boîte de réception des messages IPM, ce message est placé dans la boîte de réception, car IPM. Note. MyDocument dérive de la classe de base IPM.</span><span class="sxs-lookup"><span data-stu-id="8eeab-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="8eeab-112">Lorsque vous affectez un dossier de réception pour les messages IPC, n'utilisez jamais un dossier de la sous-arborescence IPM.</span><span class="sxs-lookup"><span data-stu-id="8eeab-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="8eeab-113">Ces dossiers doivent être réservés uniquement pour les messages IPM.</span><span class="sxs-lookup"><span data-stu-id="8eeab-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="8eeab-114">Utilisez à la place un dossier qui se trouve dans le dossier racine de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8eeab-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="8eeab-115">**Pour créer un dossier de réception pour une classe de message IPM**</span><span class="sxs-lookup"><span data-stu-id="8eeab-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="8eeab-116">Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la Banque de messages pour extraire la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8eeab-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="8eeab-117">Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) avec **PR_IPM_SUBTREE_ENTRYID** comme identificateur d'entrée pour ouvrir le dossier racine de la sous-arborescence IPM dans la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8eeab-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="8eeab-118">Appelez [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) pour créer le dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="8eeab-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="8eeab-119">Appelez [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) pour mapper le nouveau dossier sur votre classe de message IPM.</span><span class="sxs-lookup"><span data-stu-id="8eeab-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="8eeab-120">**Pour créer un dossier de réception pour une classe de message IPC**</span><span class="sxs-lookup"><span data-stu-id="8eeab-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="8eeab-121">Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) avec un identificateur d'entrée null pour ouvrir le dossier racine de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="8eeab-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="8eeab-122">Appelez [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) pour créer le dossier de réception.</span><span class="sxs-lookup"><span data-stu-id="8eeab-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="8eeab-123">Appelez [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) pour mapper le nouveau dossier à votre classe de message IPC.</span><span class="sxs-lookup"><span data-stu-id="8eeab-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="8eeab-124">Affectez le dossier de réception que vous utilisez pour les messages de rapport associés.</span><span class="sxs-lookup"><span data-stu-id="8eeab-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="8eeab-125">Par exemple, si votre client reçoit IPM. Notez les messages, configurez un dossier de réception pour l'IPM. Notez les messages et le même dossier de réception pour les messages Report. IPM. note.</span><span class="sxs-lookup"><span data-stu-id="8eeab-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

