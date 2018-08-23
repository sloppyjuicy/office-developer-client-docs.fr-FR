---
title: L’ouverture d’un descripteur d’affichage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 680d80c0827399f3b7a0ea5819e51be654a05810
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592478"
---
# <a name="opening-a-view-descriptor"></a>L’ouverture d’un descripteur d’affichage
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Nombre de dossiers peut être ouvert avec n’importe quel nombre de vues personnalisées, une vue par défaut ou un affichage normal. Un affichage explique comment afficher le contenu d’un dossier. L’affichage normal est utilisé lorsqu’il n’existe aucune autre vue et lorsque vous ouvrez le dossier pour la première fois. Lorsqu’une autre vue n’existe pas, vous devez l’utiliser pour ouvrir le dossier.
  
Une vue est décrit dans un message appelé descripteur d’un affichage. Affichage descripteurs sont généralement créés en tant que messages associés et susceptibles d’apparaître dans soit les dossiers d’affichage communs ou personnel ou dans n’importe quel dossier IPM.
  
### <a name="to-open-a-view-descriptor"></a>Pour ouvrir un descripteur d’affichage
  
1. Appelez [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) pour récupérer la table des matières associée pour le dossier. 
    
2. Créer une restriction qui localise uniquement les messages avec la classe de message réservée pour les descripteurs de vue et appelez [IMAPITable](imapitable-restrict.md) pour limiter la table et [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer les lignes appropriées, ou...
    
   Appeler [IMAPIProp::GetProps](imapiprop-getprops.md) méthode du dossier pour récupérer la propriété **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)). **PR_DEFAULT_VIEW_ENTRYID** contient l’identificateur d’entrée du message contenant le descripteur d’affichage par défaut pour un dossier. Cet appel va réussir si le dossier prend en charge l’utilisation de l’indicateur MAPI_ASSOCIATED sur les appels à [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) et [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
3. Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) avec l’identificateur d’entrée du descripteur d’affichage pour l’ouvrir. 
    

