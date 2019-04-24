---
title: Ouverture d’un descripteur de vue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1940feb0-9e0f-4d96-9fb9-b9a35a0aa661
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ce53e5a91f6fa340728872457eae7f6514e287aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326207"
---
# <a name="opening-a-view-descriptor"></a>Ouverture d’un descripteur de vue
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
De nombreux dossiers peuvent être ouverts avec un affichage normal, un affichage par défaut ou n'importe quel nombre de vues personnalisées. Une vue décrit comment afficher le contenu d'un dossier. L'affichage normal est utilisé lorsqu'il n'existe aucune autre vue ni lorsque vous ouvrez le dossier pour la première fois. Lorsqu'une autre vue existe, vous devez l'utiliser pour ouvrir le dossier.
  
Un affichage est décrit dans un message appelé descripteur de vue. Les descripteurs d'affichage sont généralement créés en tant que messages associés et peuvent apparaître dans les dossiers d'affichage courants ou personnels ou dans n'importe quel dossier IPM.
  
### <a name="to-open-a-view-descriptor"></a>Pour ouvrir un descripteur de vue
  
1. Appelez [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md) pour récupérer la table des matières associée pour le dossier. 
    
2. Créer une restriction qui localise uniquement les messages dont la classe de message est réservée pour les descripteurs de vue et appelle la fonction [IMAPITable:: Restrict](imapitable-restrict.md) pour limiter la table et la fonction [IMAPITable:: QueryRows](imapitable-queryrows.md) pour extraire les lignes appropriées, ou...
    
   Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) du dossier pour extraire sa propriété **PR_DEFAULT_VIEW_ENTRYID** ([PidTagDefaultViewEntryId](pidtagdefaultviewentryid-canonical-property.md)). **PR_DEFAULT_VIEW_ENTRYID** contient l'identificateur d'entrée pour le message contenant le descripteur d'affichage par défaut d'un dossier. Cet appel réussit si le dossier prend en charge l'utilisation de l'indicateur MAPI_ASSOCIATED sur les appels vers [IMAPIFolder: CreateMessage](imapifolder-createmessage.md) et [IMAPIContainer:: GetContentsTable](imapicontainer-getcontentstable.md).
    
3. Appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) avec l'identificateur d'entrée du descripteur de vue pour l'ouvrir. 
    

