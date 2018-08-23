---
title: Dossiers de recherche MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b5a95ca77496c3c4c2d28641ab649c2b4328a27c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578555"
---
# <a name="mapi-search-folders"></a><span data-ttu-id="bdbce-103">Dossiers de recherche MAPI</span><span class="sxs-lookup"><span data-stu-id="bdbce-103">MAPI Search Folders</span></span>

  
  
<span data-ttu-id="bdbce-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdbce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdbce-p101">A search-results folder holds links to messages in generic folders rather than the actual messages. Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter. Clients fill a search-results folder by setting up and applying search criteria�� rules that filter out messages with particular characteristics. Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**. **SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed.</span><span class="sxs-lookup"><span data-stu-id="bdbce-p101">A search-results folder holds links to messages in generic folders rather than the actual messages. Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter. Clients fill a search-results folder by setting up and applying search criteria — rules that filter out messages with particular characteristics. Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**. **SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed.</span></span> 
  
 <span data-ttu-id="bdbce-111">**SetSearchCriteria** identifies the messages that match the specified restriction.</span><span class="sxs-lookup"><span data-stu-id="bdbce-111">**SetSearchCriteria** identifies the messages that match the specified restriction.</span></span> <span data-ttu-id="bdbce-112">The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder.</span><span class="sxs-lookup"><span data-stu-id="bdbce-112">The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder.</span></span> <span data-ttu-id="bdbce-113">When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table.</span><span class="sxs-lookup"><span data-stu-id="bdbce-113">When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table.</span></span> <span data-ttu-id="bdbce-114">Contents tables for search-results folders contain the same columns as contents tables for generic folders.</span><span class="sxs-lookup"><span data-stu-id="bdbce-114">Contents tables for search-results folders contain the same columns as contents tables for generic folders.</span></span> <span data-ttu-id="bdbce-115">Toutefois, pour les dossiers de résultats de recherche, la propriété **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) spécifie l’identificateur d’entrée du dossier où réside le message lié.</span><span class="sxs-lookup"><span data-stu-id="bdbce-115">However, for search-results folders, the **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property specifies the entry identifier of the folder where the linked message resides.</span></span> <span data-ttu-id="bdbce-116">Search-results folders are not considered parent folders.</span><span class="sxs-lookup"><span data-stu-id="bdbce-116">Search-results folders are not considered parent folders.</span></span>
  
<span data-ttu-id="bdbce-117">Dossiers de r�sultats de recherche ont les limites suivantes :</span><span class="sxs-lookup"><span data-stu-id="bdbce-117">Search-results folders have the following limits:</span></span>
  
- <span data-ttu-id="bdbce-p103">La seule fa�on que le contenu d'un dossier de r�sultats de recherche peut �tre modifi� est via un appel � **SetSearchCriteria**. Pour plus d'informations sur l'impl�mentation de **SetSearchCriteria**, consultez l'article de la Base de connaissances [260322 : comment vers les dossiers de recherche avec la m�thode SetSearchCriteria](http://go.microsoft.com/fwlink/?LinkId=123603).</span><span class="sxs-lookup"><span data-stu-id="bdbce-p103">The only way that the contents of a search-results folder can be modified is through a call to **SetSearchCriteria**. For more information about the implementation of **SetSearchCriteria**, see Knowledge Base article [260322: How To Search Folders with the SetSearchCriteria Method](http://go.microsoft.com/fwlink/?LinkId=123603).</span></span>
    
- <span data-ttu-id="bdbce-120">Les messages ne peuvent pas �tre d�plac�s ou copi�s dans les dossiers de r�sultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="bdbce-120">Messages cannot be moved or copied into search-results folders.</span></span>
    
- <span data-ttu-id="bdbce-121">Dossiers de r�sultats de recherche ne peut pas contenir de sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="bdbce-121">Search-results folders cannot contain subfolders.</span></span> 
    
- <span data-ttu-id="bdbce-122">Les clients ne peut pas faire un dossier de r�sultats de recherche de l'objet d'une recherche.</span><span class="sxs-lookup"><span data-stu-id="bdbce-122">Clients cannot make a search-results folder the subject of a search.</span></span>
    
<span data-ttu-id="bdbce-p104">Toutefois, il est possible, pour modifier les propri�t�s d'un dossier de r�sultats de la recherche et l'utiliser pour supprimer un message. Lorsqu'un message est supprim� d'un dossier de r�sultats de recherche, elle est r�ellement supprim�e � partir du dossier r�el. Toutefois, la suppression du dossier de r�sultats de recherche proprement dite n'a aucun impact sur les messages � l'int�rieur ; ils restent dans leurs dossiers g�n�riques.</span><span class="sxs-lookup"><span data-stu-id="bdbce-p104">It is possible, however, to modify the properties of a search-results folder and use it to delete a message. When a message is deleted from a search-results folder, it is actually deleted from the real folder. However, deleting the search-results folder itself has no impact on the messages inside; they remain in their generic folders.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bdbce-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdbce-126">See also</span></span>



[<span data-ttu-id="bdbce-127">Dossiers MAPI</span><span class="sxs-lookup"><span data-stu-id="bdbce-127">MAPI Folders</span></span>](mapi-folders.md)

