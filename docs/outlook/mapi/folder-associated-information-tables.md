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
# <a name="folder-associated-information-tables"></a>Tables d’informations associées aux dossiers

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI définit l’indicateur MAPI_ASSOCIATED pour divers composants MAPI à utiliser lorsque vous travaillez avec des tables des informations associées. Chaque dossier dans une banque de messages doit avoir une table de contenu associé avec sa table de contenu standard. Applications clientes stockent des messages spéciaux dans le tableau de contenu associé d’un dossier pour contenir les formulaires et les vues. En fait, pour prendre en charge les formulaires et les vues, votre fournisseur de magasin de message doit implémenter les tables de contenu associée.
  
Pour implémenter les tables de contenu associé, votre fournisseur de magasins procédez comme suit :
  
- Prend en charge l’indicateur MAPI_ASSOCIATED dans la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) afin que les applications clientes peuvent obtenir la table de contenu associée du dossier au lieu de la table des matières standard. 
    
- Prend en charge l’indicateur MAPI_ASSOCIATED dans la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) afin que les applications clientes peuvent ajouter des messages à la table associée de contenu d’un dossier. 
    
- Définir le bit MAPI_ACCESS_CREATE_ASSOCIATED dans la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) avec des objets folder.
    
- Prend en charge l’indicateur DEL_ASSOCIATED dans la méthode [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) . 
    
- Définir le MSGFLAG_ASSOCIATED bit dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) pour les messages dans le tableau contenu associé.
    
- Exposer et répondez à la propriété **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sur les dossiers.
    
- Mettre à jour la propriété **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) sur les dossiers.
    
Il n’existe aucun bit dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) pour indiquer si votre fournisseur de magasin de message prend en charge les tables de contenu associée. Si votre fournisseur de magasin de message ne prend en charge les, elle doit retourner MAPI_E_NO_SUPPORT lorsque les applications clientes appellent une de ces méthodes avec l’indicateur MAPI_ASSOCIATED.
  
## <a name="see-also"></a>Voir aussi



[Fonctionnalit�s de la banque de messages](message-store-features.md)

