---
title: Utilisation d’une boîte de dialogue Recherche avancée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
ms.openlocfilehash: 61a6b0c93dd03c786ffbe2ce87c7fd912eedf089
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375789"
---
# <a name="using-an-advanced-search-dialog-box"></a>Utilisation d’une boîte de dialogue Recherche avancée

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains conteneurs de carnet d’adresses peuvent prendre en charge une fonctionnalité de recherche avancée qui permet aux clients d’effectuer des recherches sur des propriétés autres que **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Les conteneurs de carnet d’adresses qui prendre en charge les recherches avancées ont une propriété d’objet conteneur **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Cet objet conteneur permet d’accéder à un tableau d’affichage qui décrit la boîte de dialogue de recherche , une boîte de dialogue permettant d’entrer et de modifier les critères de recherche avancée.
  
 **Pour effectuer une recherche avancée sur un conteneur de carnet d’adresses**
  
1. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur, en spécifiant  PR_SEARCH pour la balise de propriété et IID_IMAPIContainer pour l’identificateur d’interface. 
    
2. Appelez la méthode **IMAPIProp::OpenProperty** de l’objet de recherche, en spécifiant **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) pour la balise de propriété et IID_IMAPITable pour l’identificateur d’interface. 
    
3. Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de l’objet de recherche pour établir des valeurs pour les propriétés à utiliser dans la recherche avancée. 
    
4. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de l’objet de recherche pour enregistrer les critères de recherche avancés. 
    
Cette séquence d’appels entraîne la disponible d’une restriction lorsqu’un client appelle la **méthode GetSearchCriteria** de l’objet de recherche. 
  

