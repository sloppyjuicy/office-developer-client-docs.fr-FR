---
title: Folder-Associated d’informations sur les données
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2710605feba0faafdfdc0ad1f4e3a1e3b19de999
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576281"
---
# <a name="folder-associated-information-tables"></a>Folder-Associated d’informations sur les données

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit l’indicateur MAPI_ASSOCIATED pour différents composants MAPI à utiliser lors du traitement des tables d’informations associées. Chaque dossier d’une magasin de messages doit être associé à une table des matières associée avec sa table des matières standard. Les applications clientes stockent des messages spéciaux dans la table des matières associée d’un dossier pour contenir des formulaires et des affichages. En fait, pour prendre en charge les formulaires et les affichages, votre fournisseur de magasins de messages doit implémenter des tables de contenu associées.
  
Pour implémenter les tables des matières associées, votre fournisseur de magasins doit :
  
- Prendre en charge l’indicateur MAPI_ASSOCIATED dans la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) afin que les applications clientes peuvent obtenir la table des matières associée au dossier au lieu de la table des matières standard. 
    
- Prise en charge MAPI_ASSOCIATED’indicateur dans la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) afin que les applications clientes peuvent ajouter des messages à la table des matières associée d’un dossier. 
    
- Définissez le bit MAPI_ACCESS_CREATE_ASSOCIATED dans la **propriété PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) sur les objets de dossier.
    
- Prise en charge DEL_ASSOCIATED’indicateur dans la [méthode IMAPIFolder::EmptyFolder.](imapifolder-emptyfolder.md) 
    
- Définissez MSGFLAG_ASSOCIATED bit dans la **propriété PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) pour les messages dans la table des matières associée.
    
- Exposer et répondre à la **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sur les dossiers.
    
- Conservez **la PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) sur les dossiers.
    
La propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)ne contient aucun bit pour indiquer si votre fournisseur de magasins de messages prend en charge les tables de contenu associées. Si votre fournisseur de magasin de messages ne les prend pas en charge, il doit renvoyer MAPI_E_NO_SUPPORT lorsque les applications clientes appellent l’une des méthodes ci-dessus avec l’indicateur MAPI_ASSOCIATED.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

