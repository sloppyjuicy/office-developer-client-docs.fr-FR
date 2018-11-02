---
title: Tables d’informations associées aux dossiers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9c9c75d0ae4b9fe060d6717dfa11ad418cbb715b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564646"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="1ae07-103">Tables d’informations associées aux dossiers</span><span class="sxs-lookup"><span data-stu-id="1ae07-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="1ae07-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ae07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ae07-105">MAPI définit l’indicateur MAPI_ASSOCIATED pour divers composants MAPI à utiliser lorsque vous travaillez avec des tables des informations associées.</span><span class="sxs-lookup"><span data-stu-id="1ae07-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="1ae07-106">Chaque dossier dans une banque de messages doit avoir une table de contenu associé avec sa table de contenu standard.</span><span class="sxs-lookup"><span data-stu-id="1ae07-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="1ae07-107">Applications clientes stockent des messages spéciaux dans le tableau de contenu associé d’un dossier pour contenir les formulaires et les vues.</span><span class="sxs-lookup"><span data-stu-id="1ae07-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="1ae07-108">En fait, pour prendre en charge les formulaires et les vues, votre fournisseur de magasin de message doit implémenter les tables de contenu associée.</span><span class="sxs-lookup"><span data-stu-id="1ae07-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="1ae07-109">Pour implémenter les tables de contenu associé, votre fournisseur de magasins procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1ae07-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="1ae07-110">Prend en charge l’indicateur MAPI_ASSOCIATED dans la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) afin que les applications clientes peuvent obtenir la table de contenu associée du dossier au lieu de la table des matières standard.</span><span class="sxs-lookup"><span data-stu-id="1ae07-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="1ae07-111">Prend en charge l’indicateur MAPI_ASSOCIATED dans la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) afin que les applications clientes peuvent ajouter des messages à la table associée de contenu d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="1ae07-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="1ae07-112">Définir le bit MAPI_ACCESS_CREATE_ASSOCIATED dans la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) avec des objets folder.</span><span class="sxs-lookup"><span data-stu-id="1ae07-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="1ae07-113">Prend en charge l’indicateur DEL_ASSOCIATED dans la méthode [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="1ae07-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="1ae07-114">Définir le MSGFLAG_ASSOCIATED bit dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) pour les messages dans le tableau contenu associé.</span><span class="sxs-lookup"><span data-stu-id="1ae07-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="1ae07-115">Exposer et répondez à la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sur les dossiers.</span><span class="sxs-lookup"><span data-stu-id="1ae07-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="1ae07-116">Mettre à jour la propriété **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) sur les dossiers.</span><span class="sxs-lookup"><span data-stu-id="1ae07-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="1ae07-117">Il n’existe aucun bit dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour indiquer si votre fournisseur de magasin de message prend en charge les tables de contenu associée.</span><span class="sxs-lookup"><span data-stu-id="1ae07-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="1ae07-118">Si votre fournisseur de magasin de message ne prend en charge les, elle doit retourner MAPI_E_NO_SUPPORT lorsque les applications clientes appellent une de ces méthodes avec l’indicateur MAPI_ASSOCIATED.</span><span class="sxs-lookup"><span data-stu-id="1ae07-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1ae07-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ae07-119">See also</span></span>



[<span data-ttu-id="1ae07-120">Fonctionnalit�s de la banque de messages</span><span class="sxs-lookup"><span data-stu-id="1ae07-120">Message Store Features</span></span>](message-store-features.md)

