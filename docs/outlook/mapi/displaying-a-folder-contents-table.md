---
title: Affichage de la table des matières d’un dossier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 56847283afaf41c1d45cdb875ddf49eaa5881175
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412393"
---
# <a name="displaying-a-folder-contents-table"></a>Affichage de la table des matières d’un dossier

**S’applique à** : Outlook 2013 | Outlook 2016 
  
La table de contenu d'un dossier contient des informations récapitulatives sur tous ses messages. Des informations récapitulatives sur les nouveaux messages entrants s'affichent dans la table des matières du dossier de réception de la classe de message. Pour mettre ces informations à la disposition des utilisateurs, récupérez la table et affichez les colonnes et les lignes, le cas échéant.
  
**Pour afficher un tableau de contenu de dossier**
  
1. Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md), en transmettant l'identificateur d'entrée du dossier contenant la table.
    
2. Appelez la méthode [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) du dossier pour ouvrir sa table des matières. 
    
3. Limitez l'affichage de la table de contenu si vous le souhaitez en appelant la méthode [IMAPITable:: SetColumns](imapitable-setcolumns.md) de la table pour spécifier des colonnes particulières. 
    
4. Limitez l'affichage de la table de contenu si vous le souhaitez en appelant la méthode [IMAPITable:: Restrict](imapitable-restrict.md) pour filtrer des lignes spécifiques. Par exemple, si vous souhaitez n'afficher que les messages avec une classe de message spécifique qui n'ont pas encore été lues: 
    
    1. Créez une restriction de propriété dans une structure [SPropertyRestriction](spropertyrestriction.md) qui correspond à la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) avec la classe de message souhaitée. 
        
    2. Créez une restriction de masque de masques dans une structure [SBitMaskRestriction](sbitmaskrestriction.md) qui utilise **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) comme balise de propriété et la valeur MSGFLAG_UNREAD comme masque.
        
    3. Créer une restriction dans une structure [SAndRestriction](sandrestriction.md) qui joint les restrictions de propriété et de masque de masque. 
    
5. Triez le tableau de contenu si vous le souhaitez en appelant la méthode [IMAPITable:: SortTable](imapitable-sorttable.md) . 
    
6. Appelez [IMAPITable:: QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes de la table de contenu pour traitement. 
    

