---
title: Écriture d’une visionneuse de hiérarchies
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
ms.openlocfilehash: 7944aa3d17b68e5b72e292adc6aede699d01d02c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379282"
---
# <a name="writing-a-hierarchy-viewer"></a>Écriture d’une visionneuse de hiérarchies

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une visionneuse de hiérarchies est un composant d’interface utilisateur utilisé pour afficher des tables de hiérarchie de conteneur de dossiers et de carnets d’adresses. Les visionneuses de hiérarchie peuvent afficher les membres de la hiérarchie à différents niveaux, en ex expandant et en contractant chaque niveau à la demande.
  
La propriété conteneur, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), contrôle le niveau d’affichage d’un membre de hiérarchie. Les entrées qui représentent des conteneurs ou des dossiers de carnet d’adresses de niveau supérieur ont leur propriété **PR_DEPTH** définie sur zéro. La valeur de cette propriété est incrémentée de manière séquentielle pour les entrées dans les niveaux séquentiels. En d’autres cas, lorsqu’un utilisateur sélectionne un conteneur de niveau supérieur à développer, affiche tous les conteneurs dont la **PR_DEPTH est définie** sur 1. Lorsqu’un utilisateur développe l’un de ces sous-ensembles, affichez les conteneurs dont la **PR_DEPTH est définie** sur 2, etc. 
  
Les visionneuses de hiérarchies supportent une plage de profondeurs différente. Vous pouvez limiter votre visionneuse à un ou deux niveaux ou vous pouvez prendre en charge plusieurs niveaux si l’affichage d’une hiérarchie étendue est une priorité. 
  
Le carnet d’adresses fournit une visionneuse de hiérarchie pour les conteneurs de niveau supérieur dans le carnet d’adresses. 
  
 **Pour accéder à la table de hiérarchie du carnet d’adresses**
  
1. [Appelez IAddrBook::OpenEntry](iaddrbook-openentry.md), en passant un identificateur d’entrée Null, pour ouvrir le conteneur racine du carnet d’adresses.
    
2. Appelez la méthode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du conteneur racine pour accéder à la table hiérarchique du carnet d’adresses MAPI. 
    
 **Pour accéder à la table de hiérarchie de la boutique de messages par défaut**
  
1. [Appelez IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) pour accéder à la table de la boutique de messages. 
    
2. Créez une restriction à l’aide de la structure [SPropertyRestriction](spropertyrestriction.md) pour limiter le tableau aux seules lignes dont la propriété **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) est définie sur TRUE. 
    
3. [Appelez IMAPITable::FindRow](imapitable-findrow.md), en lui passant **le SPropertyRestriction**, pour localiser la ligne représentant la magasin de messages par défaut. 
    
4. Appelez [IMAPISession::OpenEntry](imapisession-openentry.md), en passant la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne de la magasin de messages par défaut dans la table de la boutique de messages.
    
5. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de la boutique de messages pour récupérer la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
6. Appelez la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) de la boutique de messages, en passant la propriété **PR_IPM_SUBTREE_ENTRYID** , pour ouvrir le dossier racine de la sous-arbre IPM de la boutique de messages. 
    
7. Appelez la méthode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du dossier racine IPM pour accéder à sa table hiérarchique. 
    

