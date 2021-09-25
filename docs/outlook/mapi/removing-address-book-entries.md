---
title: Suppression d’entrées du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ea2671ecdafc5a3cc0445a510613a5eab3dac813
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609669"
---
# <a name="removing-address-book-entries"></a>Suppression d’entrées du carnet d’adresses
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La méthode [IABContainer::D eleteEntries](iabcontainer-deleteentries.md) de votre conteneur est appelée pour supprimer un ou plusieurs destinataires. **DeleteEntries a** deux paramètres : un tableau d’identificateurs d’entrée représentant les destinataires à supprimer et une valeur d’indicateurs réservés. La suppression d’un destinataire affecte la table des matières de votre conteneur . En plus de supprimer le destinataire, votre conteneur doit supprimer la ligne de table des matières qui représente le destinataire. Lorsque la ligne a été supprimée de la table, votre conteneur doit émettre une notification de table à chaque client inscrit. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Pour implémenter IABContainer::D eleteEntries
  
1. Supprimez de votre conteneur chaque destinataire représenté par l’identificateur d’entrée.
    
2. Si la table des matières de votre conteneur est ouverte :
    
   - Envoyez une notification  _fnevTableModified_ avec le membre **ulTableEvent** TABLE_ROW_DELETED aux clients inscrits pour chaque ligne de table des matières supprimée. Si votre fournisseur utilise l’utilitaire de notification, appelez [IMAPISupport::Notify](imapisupport-notify.md) pour envoyer ces notifications. 
    
   - Si votre fournisseur prend en charge les notifications d’objet, envoyez également une notification _fnevObjectDeleted._ 
    

