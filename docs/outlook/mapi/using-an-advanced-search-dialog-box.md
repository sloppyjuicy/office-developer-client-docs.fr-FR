---
title: Utilisation d’une boîte de dialogue Recherche avancée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437300"
---
# <a name="using-an-advanced-search-dialog-box"></a>Utilisation d’une boîte de dialogue Recherche avancée

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains conteneurs de carnet d’adresses peuvent prendre en charge une fonctionnalité de recherche avancée qui permet aux clients d’effectuer des recherches sur des propriétés autres que **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Les conteneurs de carnet d’adresses qui prendre en charge les recherches avancées ont une propriété d’objet conteneur **appelée PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Cet objet conteneur permet d’accéder à un tableau d’affichage qui décrit la boîte de dialogue de recherche , une boîte de dialogue utilisée pour entrer et modifier les critères de recherche avancée.
  
 **Pour effectuer une recherche avancée sur un conteneur de carnet d’adresses**
  
1. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du  conteneur, en spécifiant la PR_SEARCH de la balise de propriété et IID_IMAPIContainer l’identificateur d’interface. 
    
2. Appelez la méthode **IMAPIProp::OpenProperty** de l’objet de recherche, en spécifiant **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) pour la balise de propriété et IID_IMAPITable pour l’identificateur d’interface. 
    
3. Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de l’objet de recherche pour établir des valeurs pour les propriétés à utiliser dans la recherche avancée. 
    
4. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de l’objet de recherche pour enregistrer les critères de recherche avancés. 
    
Cette séquence d’appels entraîne la disponible d’une restriction lorsqu’un client appelle la **méthode GetSearchCriteria** de l’objet de recherche. 
  

