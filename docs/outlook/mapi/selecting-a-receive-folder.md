---
title: Sélection d’un dossier de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a4245b5dd1b70d4cf695190c65b447cf92566ef7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574481"
---
# <a name="selecting-a-receive-folder"></a>Sélection d’un dossier de réception

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un dossier de réception est l’emplacement des messages entrants d’une classe particulière. Pour IPM et les messages d’état connexes, MAPI affecte la boîte de réception comme le dossier de réception par défaut. Pour IPC et les messages d’état connexes, MAPI attribue le dossier racine de la banque de messages comme dossier de réception par défaut. Vous pouvez modifier ces affectations ou effectuer des affectations supplémentaires pour d’autres classes de message. Émission explicites recevoir des affectations de dossiers pour votre client pris en charge par message classes est facultative.
  
Lorsqu’une classe de message entrant n’a pas d’un dossier de réception affecté, le fournisseur de banque de messages utilise automatiquement le dossier de réception pour la classe qui correspond à la plus long préfixe possible de la classe entrant. Par exemple, si votre client reçoit un message de la classe IPM. Recevoir des Note.MyDocument et le seul dossier qui a été établie est la boîte de réception des messages IPM, ce message est placé dans la boîte de réception car IPM. Note.MyDocument dérive de la classe de base IPM.
  
Lorsque vous affectez un dossier de réception des messages IPC, jamais utiliser un dossier à partir de la sous-arborescence IPM. Ces dossiers doivent être réservés pour que les messages IPM. Utilisez plutôt un dossier qui se trouve dans le dossier racine de la banque messages. 
  
 **Pour créer un dossier de réception pour une classe de message IPM**
  
1. Appeler la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages pour récupérer la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)). 
    
2. Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) avec **PR_IPM_SUBTREE_ENTRYID** en tant que l’identificateur d’entrée pour ouvrir le dossier racine de la sous-arborescence IPM dans la banque de messages. 
    
3. Appelez [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) pour créer le dossier de réception. 
    
4. Appelez [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) pour mapper le nouveau dossier à votre classe de message IPM. 
    
 **Pour créer un dossier de réception pour une classe de message IPC**
  
1. Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) avec un identificateur d’entrée null pour ouvrir le dossier racine de la banque de messages. 
    
2. Appelez [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) pour créer le dossier de réception. 
    
3. Appelez [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) pour mapper le nouveau dossier à votre classe de message IPC. 
    
Affecter le dossier de réception que vous utilisez pour les messages pour les messages d’état connexes. Par exemple, si votre client reçoit IPM. Remarques, définir un dossier de réception pour futur IPM. Remarques et le même dossier des futurs messages Report.IPM.Note de réception.
  

