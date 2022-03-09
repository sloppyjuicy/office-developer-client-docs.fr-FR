---
title: Suppression d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
ms.openlocfilehash: 1a250143d7f2930fa81115a4c3d2dfe2819e49d3
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382173"
---
# <a name="deleting-a-message"></a>Suppression d’un message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un client peut supprimer un message lorsqu’il est ouvert et que l’utilisateur le lit, ou lorsqu’il est fermé et que l’utilisateur affiche la table des matières. Pour protéger un utilisateur contre la suppression accidentelle d’un message, MAPI définit la suppression des messages comme un processus en deux étapes :
  
1. Marquez un message pour suppression en le déplaçant vers le dossier désigné comme dossier Éléments supprimés , le dossier dont l’identificateur d’entrée est stocké dans la propriété **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)). 
    
2. Supprimez le message en appelant [la méthode IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md) . 
    
Lorsqu’un utilisateur choisit de supprimer un message dans un dossier autre que le dossier Éléments supprimés, marquez-le pour suppression. Ce n’est que lorsqu’un utilisateur sélectionne des messages à partir du dossier Éléments supprimés que les messages doivent être physiquement supprimés de la station de travail. Vous pouvez invite l’utilisateur à vérifier qu’il a vraiment l’intention d’effectuer la suppression.
  
 **Pour supprimer un message**
  
1. Confirmez auprès de l’utilisateur que la suppression imminente est intentionnelle.
    
2. Déterminez le parent du dossier à supprimer. S’il s’agit du dossier Éléments supprimés ou d’un sous-dossier dans le dossier Éléments supprimés, appelez [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md) pour supprimer le message. 
    
3. Si le dossier n’est pas contenu dans le dossier Éléments supprimés, appelez [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) avec l’indicateur MESSAGE_MOVE pour déplacer le message vers le dossier Éléments supprimés. 
    

