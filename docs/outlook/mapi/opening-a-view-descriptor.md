---
title: Ouverture d’un descripteur de vue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d510d1f016da2214c46aadd918a7e3cae1804379
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625146"
---
# <a name="opening-a-view-descriptor"></a>Ouverture d’un descripteur de vue
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
De nombreux dossiers peuvent être ouverts avec un affichage normal, un affichage par défaut ou un nombre quelconque d’affichages personnalisés. Un affichage décrit comment afficher le contenu d’un dossier. L’affichage normal est utilisé lorsqu’il n’existe aucune autre vue et lorsque vous ouvrent le dossier pour la première fois. Lorsqu’une autre vue existe, vous devez l’utiliser pour ouvrir le dossier.
  
Une vue est décrite dans un message appelé descripteur d’affichage. Les descripteurs d’affichage sont généralement créés en tant que messages associés et peuvent apparaître dans les dossiers d’affichage communs ou personnels ou dans n’importe quel dossier IPM.
  
### <a name="to-open-a-view-descriptor"></a>Pour ouvrir un descripteur d’affichage
  
1. Appelez [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) pour récupérer la table des matières associée au dossier. 
    
2. Créez une restriction qui localise uniquement les messages avec la classe de message réservée aux descripteurs d’affichage et appelez [IMAPITable::Restrict](imapitable-restrict.md) pour limiter la table et [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer les lignes appropriées, ou...
    
   Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du dossier pour récupérer sa PR_DEFAULT_VIEW_ENTRYID **(** [PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)). **PR_DEFAULT_VIEW_ENTRYID** contient l’identificateur d’entrée du message contenant le descripteur d’affichage par défaut d’un dossier. Cet appel aboutit si le dossier prend en charge l’utilisation de l’indicateur MAPI_ASSOCIATED sur les appels à [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) et [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md).
    
3. Appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) avec l’identificateur d’entrée du descripteur d’affichage pour l’ouvrir. 
    

