---
title: Ouverture d’un conteneur du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Dernière modification: 08 08, 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326578"
---
# <a name="opening-an-address-book-container"></a>Ouverture d’un conteneur du carnet d’adresses

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Après avoir ouvert le carnet d'adresses intégré MAPI, ouvrez un ou plusieurs conteneurs du carnet d'adresses pour accéder aux destinataires qu'ils contiennent.
  
Pour ouvrir le conteneur de niveau supérieur du carnet d'adresses, appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md) avec un identificateur d'entrée null. 
  
Les conteneurs du carnet d'adresses peuvent être implémentés avec un accès en lecture seule ou en lecture/écriture. Les conteneurs en lecture seule sont utilisés uniquement pour la navigation. Les conteneurs en lecture/écriture peuvent être modifiés, ce qui permet aux clients de créer de nouvelles entrées et de supprimer et modifier des entrées existantes. Tous les conteneurs de carnet d'adresses personnel (Cap) sont implémentés en tant que conteneurs en lecture/écriture. 
  
Pour ouvrir un conteneur de niveau inférieur, appelez **OpenEntry** et spécifiez l'identificateur d'entrée du conteneur à ouvrir. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Ouvrir le conteneur désigné comme PAB
  
1. Appelez [IAddrBook:: GetPAB](iaddrbook-getpab.md) pour récupérer l'identificateur d'entrée du carnet d'appels. 
    
2. TransMettez cet identificateur d'entrée à [IAddrBook:: OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Ouvrir un conteneur qui n'est pas le PAB
  
1. Appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md) avec un identificateur d'entrée null pour ouvrir le conteneur racine du carnet d'adresses. 
    
2. Appelez la méthode [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) du conteneur racine pour récupérer sa table de hiérarchie, c'est-à-dire une liste de tous les conteneurs de niveau supérieur dans le carnet d'adresses. 
    
3. Si le conteneur à ouvrir est d'un type spécifique:
    
   - Créez une structure **SPropertyRestriction** avec **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) pour la balise de propriété, le type du conteneur pour la valeur de propriété et RELOP_EQ pour la relation. **PR_DISPLAY_TYPE** peut être défini sur plusieurs valeurs, parmi celles-ci: 
    
   - DT_GLOBAL pour limiter la table de hiérarchie aux conteneurs appartenant à la liste d'adresses globale.
    
   - DT_LOCAL pour limiter le tableau aux conteneurs appartenant à un carnet d'adresses local.
    
   - DT_MODIFIABLE pour limiter la table aux conteneurs pouvant être modifiés.
    
   - Créer une structure [SPropTagArray](sproptagarray.md) qui inclut **PR_ENTRYID**, **PR_DISPLAY_TYPE**et toutes les autres colonnes intéressantes. 
    
   - Appelez [HrQueryAllRows](hrqueryallrows.md), en transmettant votre restriction de propriété et votre tableau de balises de propriété. **HrQueryAllRows** renverra zéro ou plusieurs lignes, une ligne pour chaque conteneur qui appartient au type spécifié. Soyez prêt à gérer le retour d'un nombre quelconque de lignes. 
    
   - Appelez **IAddrBook:: OpenEntry** avec l'identificateur d'entrée à partir de la colonne **PR_ENTRYID** de la ligne qui représente le conteneur d'intérêt. 
    
4. Si le conteneur à ouvrir appartient à un fournisseur de carnets d'adresses spécifique:
    
   - Créez une structure [SPropertyRestriction](spropertyrestriction.md) avec **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) pour la balise de propriété, une valeur spécifique au fournisseur pour la valeur de la propriété et RELOP_EQ pour la relation. En règle générale, la valeur spécifique au fournisseur est un identificateur global unique ou un GUID. Cette valeur est publiée dans l'un des fichiers d'en-tête du fournisseur de carnet d'adresses. 
    
   - Créer une structure [SPropTagArray](sproptagarray.md) qui inclut la **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**et toutes les autres colonnes intéressantes. 
    
   - Appelez [HrQueryAllRows](hrqueryallrows.md), en transmettant votre restriction de propriété et votre tableau de balises de propriété. **HrQueryAllRows** ne renvoie aucune ligne si le fournisseur de carnet d'adresses spécifié n'est pas dans le profil. Elle peut renvoyer une ou plusieurs lignes pour les conteneurs de niveau supérieur du fournisseur, en fonction de la façon dont le fournisseur est organisé. 
    
   - Appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md) avec l'identificateur d'entrée à partir de la colonne **PR_ENTRYID** de la ligne qui représente le conteneur d'intérêt. Si le conteneur qui vous intéresse n'est pas un conteneur de niveau supérieur, recherchez le conteneur de niveau supérieur et parcourez la hiérarchie. 
    

