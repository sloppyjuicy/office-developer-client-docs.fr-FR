---
title: Sélection d'un dossier de réception
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428416"
---
# <a name="selecting-a-receive-folder"></a>Sélection d'un dossier de réception

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un dossier de réception désigne l'emplacement où les messages entrants d'une classe particulière sont placés. Pour les messages IPM et related Report, MAPI affecte la boîte de réception en tant que dossier de réception par défaut. Pour les messages IPC et les rapports connexes, MAPI affecte le dossier racine de la Banque de messages comme dossier de réception par défaut. Vous pouvez modifier ces affectations ou créer des affectations supplémentaires pour d'autres classes de message. La création d'attributions de dossiers de réception explicites pour les classes de message prises en charge par votre client est facultative.
  
Lorsqu'une classe de message entrant ne dispose pas d'un dossier de réception affecté, le fournisseur de banque de messages utilise automatiquement le dossier de réception de la classe qui correspond au plus long préfixe de la classe entrante. Par exemple, si votre client reçoit un message de la classe IPM. Note. MyDocument et le seul dossier de réception qui a été établi est la boîte de réception des messages IPM, ce message est placé dans la boîte de réception, car IPM. Note. MyDocument dérive de la classe de base IPM.
  
Lorsque vous affectez un dossier de réception pour les messages IPC, n'utilisez jamais un dossier de la sous-arborescence IPM. Ces dossiers doivent être réservés uniquement pour les messages IPM. Utilisez à la place un dossier qui se trouve dans le dossier racine de la Banque de messages. 
  
 **Pour créer un dossier de réception pour une classe de message IPM**
  
1. Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la Banque de messages pour extraire la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)). 
    
2. Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) avec **PR_IPM_SUBTREE_ENTRYID** comme identificateur d'entrée pour ouvrir le dossier racine de la sous-arborescence IPM dans la Banque de messages. 
    
3. Appelez [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) pour créer le dossier de réception. 
    
4. Appelez [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) pour mapper le nouveau dossier sur votre classe de message IPM. 
    
 **Pour créer un dossier de réception pour une classe de message IPC**
  
1. Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) avec un identificateur d'entrée null pour ouvrir le dossier racine de la Banque de messages. 
    
2. Appelez [IMAPIFolder:: CreateFolder](imapifolder-createfolder.md) pour créer le dossier de réception. 
    
3. Appelez [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) pour mapper le nouveau dossier à votre classe de message IPC. 
    
Affectez le dossier de réception que vous utilisez pour les messages de rapport associés. Par exemple, si votre client reçoit IPM. Notez les messages, configurez un dossier de réception pour l'IPM. Notez les messages et le même dossier de réception pour les messages Report. IPM. note.
  

