---
title: Écriture d'une visionneuse de hiérarchie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421129"
---
# <a name="writing-a-hierarchy-viewer"></a>Écriture d'une visionneuse de hiérarchie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une visionneuse de hiérarchie est un composant d'interface utilisateur qui permet d'afficher les tables de hiérarchie des conteneurs de dossiers et de carnet d'adresses. Les visionneuses hiérarchies peuvent afficher les membres de la hiérarchie à différents niveaux, en développant et en adjudicatrices chaque niveau à la demande.
  
La propriété Container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), contrôle le niveau auquel un membre de la hiérarchie est affiché. Les entrées qui représentent des conteneurs ou des dossiers de carnet d'adresses de niveau supérieur ont leur propriété **PR_DEPTH** définie sur zéro. La valeur de cette propriété est incrémentée de manière séquentielle pour les entrées dans des niveaux séquentiels. Autrement dit, lorsqu'un utilisateur sélectionne un conteneur de niveau supérieur, affichez tous les conteneurs avec **PR_DEPTH** défini sur 1. Lorsqu'un utilisateur développe l'un de ces sous-conteneurs, affiche les conteneurs avec **PR_DEPTH** défini sur 2, et ainsi de suite. 
  
Les visualiseurs de hiérarchie prennent en charge une plage de profondeurs différente. Vous pouvez limiter votre visionneuse à un ou deux niveaux, ou vous pouvez prendre en charge plusieurs niveaux, si l'affichage d'une hiérarchie trop vaste est une priorité. 
  
Le carnet d'adresses fournit une visionneuse de hiérarchie pour les conteneurs de niveau supérieur dans le carnet d'adresses. 
  
 **Pour accéder à la table de hiérarchie de carnets d'adresses**
  
1. Appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md), en transmettant un identificateur d'entrée null, pour ouvrir le conteneur racine du carnet d'adresses.
    
2. Appelez la méthode [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) du conteneur racine pour accéder à la table de hiérarchie du carnet d'adresses MAPI. 
    
 **Pour accéder à la table de hiérarchie de la Banque de messages par défaut**
  
1. Appelez [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) pour accéder à la table de banque de messages. 
    
2. Créez une restriction à l'aide de la structure [SPropertyRestriction](spropertyrestriction.md) pour limiter la table aux seules lignes dont la propriété **PR_DEFAULT_STORE** ([PIDTAGDEFAULTSTORE](pidtagdefaultstore-canonical-property.md)) a la valeur true. 
    
3. Appelez [IMAPITable:: FindRow](imapitable-findrow.md), en lui transmettant le **SPropertyRestriction**, pour localiser la ligne représentant la Banque de messages par défaut. 
    
4. Appelez [IMAPISession:: OpenEntry](imapisession-openentry.md), en transmettant la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne de la Banque de messages par défaut dans la table de banque de messages.
    
5. Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la Banque de messages pour extraire la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
6. Appelez la méthode [IMsgStore:: OpenEntry](imsgstore-openentry.md) de la Banque de messages, en passant la propriété **PR_IPM_SUBTREE_ENTRYID** , pour ouvrir le dossier racine de la sous-arborescence IPM de la Banque de messages. 
    
7. Appelez la méthode [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) du dossier racine IPM pour accéder à sa table de hiérarchie. 
    

