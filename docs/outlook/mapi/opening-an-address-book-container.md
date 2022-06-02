---
title: Ouverture d’un conteneur du carnet d’adresses
description: Après avoir ouvert le carnet d’adresses intégré MAPI, un ou plusieurs conteneurs de carnets d’adresses doivent être ouverts pour accéder aux destinataires qu’ils contiennent.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
ms.openlocfilehash: 44cd7a4e13fd9936ead9629999547d66fed84add
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65852389"
---
# <a name="opening-an-address-book-container"></a>Ouverture d’un conteneur du carnet d’adresses

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Après avoir ouvert le carnet d’adresses intégré MAPI, ouvrez un ou plusieurs conteneurs de carnets d’adresses pour accéder aux destinataires qu’ils contiennent.
  
Pour ouvrir le conteneur de niveau supérieur du carnet d’adresses, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) avec un identificateur d’entrée NULL. 
  
Les conteneurs de carnets d’adresses peuvent être implémentés avec un accès en lecture seule ou en lecture/écriture. Les conteneurs en lecture seule sont utilisés uniquement pour la navigation. Les conteneurs en lecture/écriture peuvent être modifiés, ce qui permet aux clients de créer des entrées et de supprimer et de modifier des entrées existantes. Tous les conteneurs de carnet d’adresses personnels (PAB) sont implémentés en tant que conteneurs en lecture/écriture. 
  
Pour ouvrir un conteneur de niveau inférieur, appelez **OpenEntry** et spécifiez l’identificateur d’entrée du conteneur à ouvrir. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Ouvrir le conteneur désigné comme PAB
  
1. Appelez [IAddrBook::GetPAB](iaddrbook-getpab.md) pour récupérer l’identificateur d’entrée du PAB. 
    
2. Transmettez cet identificateur d’entrée à [IAddrBook::OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Ouvrir un conteneur qui n’est pas le PAB
  
1. Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) avec un identificateur d’entrée NULL pour ouvrir le conteneur racine du carnet d’adresses. 
    
2. Appelez la méthode [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du conteneur racine pour récupérer sa table de hiérarchie , une liste de tous les conteneurs de niveau supérieur dans le carnet d’adresses. 
    
3. Si le conteneur à ouvrir est d’un type spécifique :
    
   - Créez une structure **SPropertyRestriction** avec **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) pour la balise de propriété, le type du conteneur pour la valeur de propriété et RELOP_EQ pour la relation. **PR_DISPLAY_TYPE** peuvent être définies sur de nombreuses valeurs, parmi elles : 
    
   - DT_GLOBAL de limiter la table de hiérarchie aux conteneurs qui appartiennent à la liste d’adresses globale.
    
   - DT_LOCAL de limiter la table aux conteneurs appartenant à un carnet d’adresses local.
    
   - DT_MODIFIABLE limiter la table aux conteneurs qui peuvent être modifiés.
    
   - Créez une structure [SPropTagArray](sproptagarray.md) qui inclut **PR_ENTRYID**, **PR_DISPLAY_TYPE** et toutes les autres colonnes intéressantes. 
    
   - Appelez [HrQueryAllRows](hrqueryallrows.md), en passant votre restriction de propriété et votre tableau de balises de propriétés. **HrQueryAllRows** retourne zéro ou plusieurs lignes, une ligne pour chaque conteneur qui appartient au type spécifié. Soyez prêt à gérer le retour d’un nombre quelconque de lignes. 
    
   - Appelez **IAddrBook::OpenEntry** avec l’identificateur d’entrée de la colonne **PR_ENTRYID** de la ligne qui représente le conteneur d’intérêt. 
    
4. Si le conteneur à ouvrir appartient à un fournisseur de carnet d’adresses spécifique :
    
   - Créez une structure [SPropertyRestriction](spropertyrestriction.md) avec **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) pour la balise de propriété, une valeur spécifique au fournisseur pour la valeur de propriété et RELOP_EQ pour la relation. En règle générale, la valeur spécifique au fournisseur est un identificateur global unique ou un GUID. Vous trouverez cette valeur publiée dans l’un des fichiers d’en-tête du fournisseur de carnet d’adresses. 
    
   - Créez une structure [SPropTagArray](sproptagarray.md) qui inclut **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS** et toutes les autres colonnes intéressantes. 
    
   - Appelez [HrQueryAllRows](hrqueryallrows.md), en passant votre restriction de propriété et votre tableau de balises de propriétés. **HrQueryAllRows** retourne zéro ligne si le fournisseur de carnet d’adresses spécifié ne figure pas dans le profil. Il peut retourner une ou plusieurs lignes pour les conteneurs de niveau supérieur du fournisseur, selon la façon dont le fournisseur est organisé. 
    
   - Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) avec l’identificateur d’entrée de la colonne **PR_ENTRYID** de la ligne qui représente le conteneur d’intérêt. Si le conteneur qui vous intéresse n’est pas un conteneur de niveau supérieur, recherchez le conteneur de niveau supérieur et parcourez la hiérarchie. 
    

