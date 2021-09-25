---
title: Dossiers de recherche MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 36c14d91-77f7-43a3-8d87-d50bcc21fad7
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 26ad19b28d70fb7f68115bc701536002f0c5276b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610166"
---
# <a name="mapi-search-folders"></a>Dossiers de recherche MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
A search-results folder holds links to messages in generic folders rather than the actual messages. Clients create a search-results folder by calling the [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) method with FOLDER_SEARCH as the  _ulFolderType_ parameter. Clients fill a search-results folder by setting up and applying search criteria�� rules that filter out messages with particular characteristics. Search criteria are set up with the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method. Clients build one or more [SRestriction](srestriction.md) structures to represent the search criteria to be applied and pass them to **SetSearchCriteria**. **SetSearchCriteria** also specifies a list of folders that indicate the search domain and a set of flags that control how the search is performed. 
  
 **SetSearchCriteria** identifies the messages that match the specified restriction. The selected messages (the ones that satisfy the criteria) are displayed as links in the search-results folder. When the client calls the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method to access the contents table of the search-results folder, the selected messages are displayed in the table. Contents tables for search-results folders contain the same columns as contents tables for generic folders. Toutefois, pour les dossiers de résultats de recherche, la propriété **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) spécifie l’identificateur d’entrée du dossier où réside le message lié. Search-results folders are not considered parent folders.
  
Dossiers de r�sultats de recherche ont les limites suivantes :
  
- La seule fa�on que le contenu d'un dossier de r�sultats de recherche peut �tre modifi� est via un appel � **SetSearchCriteria**. Pour plus d'informations sur l'impl�mentation de **SetSearchCriteria**, consultez l'article de la Base de connaissances [260322 : comment vers les dossiers de recherche avec la m�thode SetSearchCriteria](https://go.microsoft.com/fwlink/?LinkId=123603).
    
- Les messages ne peuvent pas �tre d�plac�s ou copi�s dans les dossiers de r�sultats de recherche.
    
- Dossiers de r�sultats de recherche ne peut pas contenir de sous-dossiers. 
    
- Les clients ne peut pas faire un dossier de r�sultats de recherche de l'objet d'une recherche.
    
Toutefois, il est possible, pour modifier les propri�t�s d'un dossier de r�sultats de la recherche et l'utiliser pour supprimer un message. Lorsqu'un message est supprim� d'un dossier de r�sultats de recherche, elle est r�ellement supprim�e � partir du dossier r�el. Toutefois, la suppression du dossier de r�sultats de recherche proprement dite n'a aucun impact sur les messages � l'int�rieur ; ils restent dans leurs dossiers g�n�riques.
  
## <a name="see-also"></a>Voir aussi



[Dossiers MAPI](mapi-folders.md)

