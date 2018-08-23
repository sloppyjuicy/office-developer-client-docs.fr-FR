---
title: Écriture d’une visionneuse de hiérarchie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6ff394c95dfa3166d39dcba4b0c577dcfac7b8d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581593"
---
# <a name="writing-a-hierarchy-viewer"></a>Écriture d’une visionneuse de hiérarchie

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une visionneuse de hiérarchie est un composant d’interface utilisateur qui est utilisé pour l’affichage des tables de hiérarchie de conteneur livre dossier et l’adresse. Visionneuses de hiérarchie peuvent afficher les membres de la hiérarchie à différents niveaux, extension et réduction de chaque niveau de la demande.
  
La propriété container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), détermine le niveau auquel un membre de la hiérarchie est affiché. Entrées qui représentent les conteneurs de carnet d’adresses de niveau supérieur ou des dossiers ont leur propriété **PR_DEPTH** définie sur zéro. La valeur de cette propriété est incrémentée dans l’ordre des entrées de niveaux séquentiels. Autrement dit, lorsqu’un utilisateur sélectionne un conteneur de niveau supérieur pour développer, afficher tous les conteneurs avec **PR_DEPTH** la valeur 1. Lorsqu’un utilisateur développe une de ces sous-conteneurs, afficher les conteneurs avec set **PR_DEPTH** à 2 et ainsi de suite. 
  
Visionneuses de hiérarchie prend en charge une plage des profondeurs différente. Vous pouvez limiter l’afficheur uniquement un ou deux niveaux ou prennent en charge plusieurs niveaux, si l’affichage d’une hiérarchie l’est une priorité. 
  
Le carnet d’adresses fournit une visionneuse de la hiérarchie pour les conteneurs de niveau supérieur dans le carnet d’adresses. 
  
 **Accès à la table de hiérarchie adresse téléchargeable**
  
1. Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md), en passant un identificateur d’entrée null, pour ouvrir le conteneur de racine du carnet d’adresses.
    
2. Appelez la méthode de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du conteneur racine pour accéder à la table de hiérarchie du carnet d’adresses MAPI. 
    
 **Pour accéder à table de hiérarchie de la banque de messages par défaut**
  
1. Appelez [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) pour accéder à la table. 
    
2. Créer une restriction à l’aide de la structure [SPropertyRestriction](spropertyrestriction.md) pour limiter la table pour que les lignes qui ont une propriété **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) la valeur TRUE. 
    
3. Appel [IMAPITable::FindRow](imapitable-findrow.md), en lui transmettant l' **SPropertyRestriction**, pour rechercher la ligne qui représente la banque de messages par défaut. 
    
4. Appelez [IMAPISession::OpenEntry](imapisession-openentry.md), en passant la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la ligne de la banque de messages par défaut dans la table.
    
5. Appeler la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages pour récupérer la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
6. Appelez la méthode de [IMsgStore::OpenEntry](imsgstore-openentry.md) de la banque de messages, en passant la propriété **PR_IPM_SUBTREE_ENTRYID** , pour ouvrir le dossier racine de la sous-arborescence IPM de la banque de messages. 
    
7. Appeler la méthode de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du dossier racine IPM pour accéder à la table de hiérarchie. 
    

