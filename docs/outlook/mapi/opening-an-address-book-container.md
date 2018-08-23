---
title: L’ouverture d’un conteneur de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Dernière modification : 08 novembre 2011'
ms.openlocfilehash: 79f1f9254e69e1871e886fa0bb3fbb66e2aab128
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590455"
---
# <a name="opening-an-address-book-container"></a>L’ouverture d’un conteneur de carnet d’adresses

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Après que l’ouverture de l’interface MAPI intégré du carnet d’adresses, ouvrez un ou plusieurs conteneurs de carnet d’adresses pour accéder à des destinataires au sein de celles-ci.
  
Pour ouvrir le conteneur de niveau supérieur du carnet d’adresses, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) avec un identificateur d’entrée NULL. 
  
Conteneurs de carnet d’adresses peuvent être implémentées en lecture seule ou l’accès en lecture/écriture. Conteneurs en lecture seule sont utilisés uniquement pour la navigation. Conteneurs de lecture/écriture peuvent être modifiées, ce qui permet aux clients de créer de nouvelles entrées et supprimer et modifier des entrées existantes. Tous les conteneurs de carnet d’adresses personnel sont implémentées en tant que conteneurs en lecture-écriture. 
  
Pour ouvrir un conteneur de niveau inférieur, appelez **OpenEntry** et spécifier l’identificateur d’entrée du conteneur à ouvrir. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Ouvrez le conteneur désigné comme le carnet d’adresses personnel
  
1. Appelez [IAddrBook::GetPAB](iaddrbook-getpab.md) pour récupérer l’identificateur d’entrée du carnet d’adresses personnel. 
    
2. Passez cet identificateur d’entrée à [IAddrBook::OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Ouvrez un conteneur qui n’est pas le carnet d’adresses personnel
  
1. Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) avec un identificateur d’entrée NULL pour ouvrir le conteneur de racine du carnet d’adresses. 
    
2. Méthode de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) du conteneur racine pour récupérer la table de hiérarchie d’appel, une liste de tous les conteneurs de niveau supérieur dans le carnet d’adresses. 
    
3. Si le conteneur à ouvrir est d’un type spécifique :
    
   - Créez une structure **SPropertyRestriction** avec **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) pour la balise de propriété, le type du conteneur pour la valeur de la propriété et RELOP_EQ pour la relation. **PR_DISPLAY_TYPE** peut être définie à plusieurs valeurs, entre eux : 
    
   - DT_GLOBAL pour limiter la table de hiérarchie aux conteneurs qui appartiennent à la liste d’adresses globale.
    
   - DT_LOCAL pour limiter la table aux conteneurs appartenant à un carnet d’adresses local.
    
   - DT_MODIFIABLE pour limiter la table aux conteneurs qui peut être modifiée.
    
   - Créez une structure [SPropTagArray](sproptagarray.md) qui inclut toutes les colonnes d’intérêt, **PR_DISPLAY_TYPE**et **PR_ENTRYID**. 
    
   - Appelez [HrQueryAllRows](hrqueryallrows.md), en transmettant votre tableau de la propriété tag et de restriction de propriété. **HrQueryAllRows** renvoie zéro ou plusieurs lignes, une ligne pour chaque conteneur qui appartient au type spécifié. Être préparé à gérer le retour de n’importe quel nombre de lignes. 
    
   - Appelez **IAddrBook::OpenEntry** avec l’identificateur d’entrée de la colonne **PR_ENTRYID** de la ligne qui représente le conteneur d’intérêt. 
    
4. Si le conteneur à ouvrir appartient à un fournisseur de carnet d’adresse spécifique :
    
   - Créez une structure [SPropertyRestriction](spropertyrestriction.md) avec **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) pour la balise de propriété, une valeur spécifique au fournisseur pour la valeur de la propriété et RELOP_EQ pour la relation. En général, la valeur spécifique au fournisseur est un identificateur global unique ou le GUID. Vous trouverez cette valeur publiée dans un des fichiers d’en-tête du fournisseur de carnet d’adresses. 
    
   - Créez une structure [SPropTagArray](sproptagarray.md) qui inclut toutes les colonnes d’intérêt, **PR_AB_PROVIDERS**et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). 
    
   - Appelez [HrQueryAllRows](hrqueryallrows.md), en transmettant votre tableau de la propriété tag et de restriction de propriété. **HrQueryAllRows** renvoie zéro lignes si le fournisseur de carnet d’adresse spécifiée n’est pas dans le profil. Elle peut renvoyer une ou plusieurs lignes pour les conteneurs de niveau supérieur du fournisseur, en fonction de l’organisation du fournisseur. 
    
   - Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) avec l’identificateur d’entrée de la colonne **PR_ENTRYID** de la ligne qui représente le conteneur d’intérêt. Si le conteneur qui vous intéressez n’est pas un conteneur de niveau supérieur, recherchez le conteneur de niveau supérieur et parcourir la hiérarchie. 
    

