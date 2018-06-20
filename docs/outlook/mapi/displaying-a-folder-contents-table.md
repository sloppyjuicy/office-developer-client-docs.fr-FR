---
title: Affichage d’une table de contenu de dossier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 14a4c123-776d-4a32-9688-8a4402dd1f53
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 30099e9fe645f810e08ba331717cff975f69b313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783190"
---
# <a name="displaying-a-folder-contents-table"></a>Affichage d’une table de contenu de dossier

**S’applique à**: Outlook 
  
La table des matières d’un dossier contient des informations récapitulatives sur tous ses messages. Informations récapitulatives concernant les nouveaux messages entrants s’affiche dans le tableau contenu du dossier de réception pour la classe de message. Pour rendre ces informations disponibles aux utilisateurs, extraire la table et afficher les colonnes et lignes comme il convient.
  
**Pour afficher un tableau contenu de dossier**
  
1. Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md), en passant l’identificateur d’entrée du dossier contenant la table.
    
2. Appelez du dossier [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) pour ouvrir la table des matières. 
    
3. Limiter l’affichage de la table des matières si vous le souhaitez en appelant la méthode [IMAPITable::SetColumns](imapitable-setcolumns.md) de la table pour spécifier les colonnes particuliers. 
    
4. Limiter l’affichage de la table des matières si vous le souhaitez en appelant la méthode la table [IMAPITable](imapitable-restrict.md) pour filtrer les lignes particuliers. Si, par exemple, vous souhaitez afficher uniquement les messages avec une classe de message spécifique qui n’ont pas encore être lues : 
    
    1. Créez une restriction de propriété dans une structure [SPropertyRestriction](spropertyrestriction.md) qui correspond à la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) avec la classe de message de votre choix. 
        
    2. Créez une restriction de masque de bits dans une structure [SBitMaskRestriction](sbitmaskrestriction.md) qui utilise **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) en tant que la balise de propriété et la valeur MSGFLAG_UNREAD comme masque.
        
    3. Créez une restriction dans une structure [SAndRestriction](sandrestriction.md) qui associe les restrictions de propriété et masque de bits. 
    
5. Trier le tableau contenu si vous le souhaitez en appelant la méthode [IMAPITable::SortTable](imapitable-sorttable.md) de la table. 
    
6. [IMAPITable::QueryRows](imapitable-queryrows.md) pour extraire toutes les lignes de la table de contenu pour le traitement des appels. 
    

