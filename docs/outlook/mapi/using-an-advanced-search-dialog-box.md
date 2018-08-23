---
title: Utilisation d’une boîte de dialogue de recherche avancée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 581607e184d67413e735c4cbfb874643b3222a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588768"
---
# <a name="using-an-advanced-search-dialog-box"></a>Utilisation d’une boîte de dialogue de recherche avancée

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Certains conteneurs de carnet d’adresses prend en charge une fonction de recherche avancée qui permet aux clients d’effectuer une recherche sur les propriétés de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Conteneurs du carnet d’adresses qui prennent en charge les recherches avancées ont une propriété de l’objet conteneur appelée **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Cet objet conteneur fournit l’accès à un tableau d’affichage qui décrit la boîte de dialogue de recherche — une boîte de dialogue permet d’entrer et de modifier les critères de recherche avancée.
  
 **Pour effectuer une recherche avancée sur un conteneur de carnet d’adresses**
  
1. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur spécifiant **PR_SEARCH** pour la balise de propriété et IID_IMAPIContainer pour l’identificateur d’interface. 
    
2. Appeler la méthode **IMAPIProp::OpenProperty** de l’objet de la recherche, spécification **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) pour la balise de propriété et IID_IMAPITable pour l’identificateur d’interface. 
    
3. Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de l’objet de la recherche pour définir des valeurs pour les propriétés à utiliser dans la recherche avancée. 
    
4. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de l’objet de la recherche pour enregistrer les critères de recherche avancée. 
    
Cette séquence d’appels entraîne une restriction étant disponible lorsqu’un client appelle la méthode **GetSearchCriteria** de l’objet de la recherche. 
  

