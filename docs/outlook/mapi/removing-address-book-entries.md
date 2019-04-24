---
title: Suppression d’entrées du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328349"
---
# <a name="removing-address-book-entries"></a>Suppression d’entrées du carnet d’adresses
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
IABContainer de votre conteneur: la méthode [eleteentries:D](iabcontainer-deleteentries.md) est appelée pour supprimer un ou plusieurs destinataires. **DeleteEntries** comporte deux paramètres: un tableau d'identificateurs d'entrée représentant les destinataires à supprimer et une valeur d'indicateurs réservée. La suppression d'un destinataire affecte la table des matières de votre conteneur; en plus de supprimer le destinataire, votre conteneur doit supprimer la ligne de la table de contenu qui représente le destinataire. Lorsque la ligne a été supprimée de la table, votre conteneur doit émettre une notification de table pour chaque client inscrit. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Pour implémenter IABContainer, procédez comme suit::D eleteEntries
  
1. Supprimez tous les destinataires représentés par l'identificateur d'entrée de votre conteneur.
    
2. Si la table des matières de votre conteneur est ouverte:
    
   - Envoyez une notification _fnevTableModified_ avec le membre **ULTABLEEVENT** défini sur TABLE_ROW_DELETED aux clients inscrits pour chaque ligne de tableau de contenu supprimé. Si votre fournisseur utilise l'utilitaire de notification, appelez [IMAPISupport:: Notify](imapisupport-notify.md) pour envoyer ces notifications. 
    
   - Si votre fournisseur prend en charge les notifications d'objet, envoyez également une notification _fnevObjectDeleted_ . 
    

