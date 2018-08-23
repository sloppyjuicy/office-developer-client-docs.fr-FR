---
title: Suppression d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ad891a9884e72aa352dc114232cd5951c590272f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585100"
---
# <a name="deleting-a-message"></a>Suppression d’un message

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un client peut supprimer un message lorsqu’il est ouvert et que l’utilisateur est le lire, ou lorsqu’elle est fermée et l’utilisateur visualise la table des matières. Pour empêcher un utilisateur de suppression par inadvertance d’un message, MAPI définit la suppression des messages sous la forme d’un processus en deux étapes :
  
1. Marquer un message de suppression en les déplaçant vers le dossier qui a été désigné en tant que le dossier éléments supprimés, le dossier dont l’identificateur de l’entrée est stockée dans la propriété **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)). 
    
2. Supprimer le message en appelant la méthode [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) . 
    
Lorsqu’un utilisateur choisit supprimer un message dans un dossier autre que le dossier éléments supprimés, marquer pour la suppression. Uniquement lorsqu’un utilisateur sélectionne des messages à partir du dossier éléments supprimés doivent les messages d’être physiquement retirés de la station de travail. Vous pouvez inviter l’utilisateur à vérifier que l’utilisateur prévu effectuer la suppression.
  
 **Pour supprimer un message**
  
1. Avec l’utilisateur, vérifiez que la suppression imminente est intentionnelle.
    
2. Déterminer le parent du dossier à supprimer. Si c’est le dossier éléments supprimés ou un sous-dossier dans le dossier éléments supprimés, appelez [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) pour supprimer le message. 
    
3. Si le dossier n’est pas contenu dans le dossier éléments supprimés, appelez [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) avec l’indicateur MESSAGE_MOVE pour déplacer le message vers le dossier éléments supprimés. 
    

