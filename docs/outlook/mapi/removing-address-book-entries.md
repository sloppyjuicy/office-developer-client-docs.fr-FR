---
title: Suppression des entrées de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1fb7224e110bbee6844cf2820782aac8be213ba3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786979"
---
# <a name="removing-address-book-entries"></a>Suppression des entrées de carnet d’adresses
  
**S’applique à**: Outlook 
  
Méthode de [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) de votre conteneur est appelée pour supprimer un ou plusieurs destinataires. **DeleteEntries** possède deux paramètres : un tableau d’identificateurs d’entrée représentant les destinataires à supprimer et une valeur pour les indicateurs réservés. Suppression d’un destinataire affecte la table des matières de votre conteneur ; en plus de supprimer le destinataire, le conteneur doit supprimer la ligne du tableau contenu qui représente le destinataire. Lorsque la ligne a été supprimée de la table, votre conteneur doit émettre une notification de la table pour chaque client enregistré. 
  
### <a name="to-implement-iabcontainerdeleteentries"></a>Pour mettre en œuvre IABContainer::DeleteEntries
  
1. Supprimez chaque destinataire représentée par l’identificateur d’entrée à partir de votre conteneur.
    
2. Si la table des matières de votre conteneur est ouvert :
    
   - Envoyer une notification _fnevTableModified_ avec le membre **ulTableEvent** défini sur TABLE_ROW_DELETED aux clients enregistrés pour chaque ligne du tableau contenu supprimé. Si votre fournisseur utilise l’utilitaire de notification, appelez [IMAPISupport::Notify](imapisupport-notify.md) pour envoyer ces notifications. 
    
   - Si votre fournisseur prend en charge les notifications de l’objet, également envoyer une notification _fnevObjectDeleted_ . 
    

