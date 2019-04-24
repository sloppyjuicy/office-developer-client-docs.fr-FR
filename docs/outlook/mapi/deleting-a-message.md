---
title: Suppression d'un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 663eebfcd1b8862b22d8c822957024c4f31499de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316834"
---
# <a name="deleting-a-message"></a>Suppression d'un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un client peut supprimer un message lorsqu'il est ouvert et que l'utilisateur le lit, ou lorsqu'il est fermé et que l'utilisateur affiche la table des matières. Pour empêcher un utilisateur de supprimer un message par inadvertance, MAPI définit la suppression des messages comme un processus en deux étapes:
  
1. Marquer un message pour suppression en le dépositionnant vers le dossier désigné comme dossier éléments supprimés — le dossier dont l'identificateur d'entrée est stocké dans la propriété **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)). 
    
2. Supprimez le message en appelant la méthode [IMAPIFolder::D eletemessages](imapifolder-deletemessages.md) . 
    
Lorsqu'un utilisateur choisit de supprimer un message dans un dossier autre que le dossier éléments supprimés, marquez-le pour suppression. Uniquement lorsqu'un utilisateur sélectionne des messages dans le dossier éléments supprimés si les messages doivent être supprimés physiquement de la station de travail. Vous pouvez inviter l'utilisateur à vérifier que l'utilisateur a réellement prévu d'effectuer la suppression.
  
 **Pour supprimer un message**
  
1. Vérifiez auprès de l'utilisateur que la suppression imminente est intentionnelle.
    
2. Déterminez le parent du dossier à supprimer. S'il s'agit du dossier éléments supprimés ou d'un sous-dossier dans le dossier éléments supprimés, appelez [IMAPIFolder::D eletemessages](imapifolder-deletemessages.md) pour supprimer le message. 
    
3. Si le dossier n'est pas contenu dans le dossier éléments supprimés, appelez [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) avec l'indicateur MESSAGE_MOVE défini pour déplacer le message vers le dossier éléments supprimés. 
    

