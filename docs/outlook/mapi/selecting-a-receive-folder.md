---
title: Sélection d’un dossier de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
ms.openlocfilehash: ab9b569871ea09c24d55cc97d75860e420eb6bd7
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374865"
---
# <a name="selecting-a-receive-folder"></a>Sélection d’un dossier de réception

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un dossier de réception est l’endroit où les messages entrants d’une classe particulière sont placés. Pour les messages de rapport IPM et associés, MAPI affecte la boîte de réception comme dossier de réception par défaut. Pour les messages de rapport IPC et associés, MAPI affecte le dossier racine de la magasin de messages comme dossier de réception par défaut. Vous pouvez modifier ces affectations ou effectuer des affectations supplémentaires pour d’autres classes de messages. Il est facultatif d’effectuer des attributions de dossier de réception explicites pour les classes de messages pris en charge par votre client.
  
Lorsqu’une classe de message entrante n’a pas de dossier de réception affecté, le fournisseur de magasin de messages utilise automatiquement le dossier de réception pour la classe qui correspond au préfixe le plus long possible de la classe entrante. Par exemple, si votre client reçoit un message de classe IPM. Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM. Note.MyDocument dérive de la classe de base IPM.
  
Lorsque vous affectez un dossier de réception pour les messages IPC, n’utilisez jamais de dossier de la sous-arbre IPM. Ces dossiers doivent être réservés aux messages IPM uniquement. Utilisez plutôt un dossier contenu dans le dossier racine de la boutique de messages. 
  
 **Pour créer un dossier de réception pour une classe de message IPM**
  
1. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la boutique de messages pour récupérer la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)). 
    
2. Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) avec **PR_IPM_SUBTREE_ENTRYID** comme identificateur d’entrée pour ouvrir le dossier racine de la sous-arbre IPM dans la magasin de messages. 
    
3. [Appelez IMAPIFolder::CreateFolder](imapifolder-createfolder.md) pour créer le dossier de réception. 
    
4. [Appelez IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) pour maquer le nouveau dossier sur votre classe de message IPM. 
    
 **Pour créer un dossier de réception pour une classe de message IPC**
  
1. [Appelez IMsgStore::OpenEntry avec un identificateur](imsgstore-openentry.md) d’entrée Null pour ouvrir le dossier racine de la magasin de messages. 
    
2. [Appelez IMAPIFolder::CreateFolder](imapifolder-createfolder.md) pour créer le dossier de réception. 
    
3. [Appelez IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) pour maquer le nouveau dossier sur votre classe de message IPC. 
    
Attribuez le dossier de réception que vous utilisez pour les messages de rapport associés. Par exemple, si votre client reçoit un IPM. Note messages, set up one receive folder for future IPM. Note messages and the same receive folder for future Report.IPM.Note messages.
  

