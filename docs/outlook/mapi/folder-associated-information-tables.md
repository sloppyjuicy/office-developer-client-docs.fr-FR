---
title: Tables d'informations associées aux dossiers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426414"
---
# <a name="folder-associated-information-tables"></a>Tables d'informations associées aux dossiers

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit l'indicateur MAPI_ASSOCIATED pour divers composants MAPI à utiliser lors du traitement des tables d'informations associées. Chaque dossier dans une banque de messages doit être associé à une table de contenu associée à la table de contenu standard. Les applications clientes stockent des messages spéciaux dans le tableau de contenu associé d'un dossier pour contenir des formulaires et des vues. En fait, pour prendre en charge les formulaires et les vues, votre fournisseur de banque de messages doit implémenter les tables de contenu associées.
  
Pour implémenter les tables de contenu associées, votre fournisseur de banque doit effectuer les opérations suivantes:
  
- Prendre en charge l'indicateur MAPI_ASSOCIATED dans la méthode [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) afin que les applications clientes puissent obtenir la table des matières associée du dossier au lieu de la table des matières standard. 
    
- Prendre en charge l'indicateur MAPI_ASSOCIATED dans la méthode [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) afin que les applications clientes puissent ajouter des messages à la table des matières associée d'un dossier. 
    
- Définissez le bit MAPI_ACCESS_CREATE_ASSOCIATED dans la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) sur les objets Folder.
    
- Prendre en charge l'indicateur DEL_ASSOCIATED dans la méthode [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md) . 
    
- Définissez le bit MSGFLAG_ASSOCIATED dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) pour les messages dans le tableau des contenus associés.
    
- ExPosez et répondez à la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sur les dossiers.
    
- Conservez la propriété **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) sur les dossiers.
    
Il n'y a pas de bit dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour indiquer si votre fournisseur de banque de messages prend en charge les tables de contenu associées. Si votre fournisseur de banque de messages ne les prend pas en charge, il doit renvoyer MAPI_E_NO_SUPPORT lorsque les applications clientes appellent l'une des méthodes ci-dessus avec l'indicateur MAPI_ASSOCIATED.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

