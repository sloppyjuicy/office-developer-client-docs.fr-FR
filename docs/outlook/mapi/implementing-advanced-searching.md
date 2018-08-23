---
title: Implémentation de la recherche avancée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0ba9958588c476ae330b0f4a413361e80d54667a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571968"
---
# <a name="implementing-advanced-searching"></a>Implémentation de la recherche avancée

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Certains conteneurs de carnet d’adresses prend en charge une fonction de recherche avancée qui permet aux clients d’effectuer une recherche sur les propriétés de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Pour prendre en charge les recherches avancées, votre fournisseur doit implémenter un conteneur spécial qui est accessible via la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de vos autres conteneurs. **PR_SEARCH** contient un objet conteneur qui fournit l’accès à un tableau d’affichage qui décrit la boîte de dialogue permet d’entrer et de modifier les critères de recherche avancée. 
  
 **Pour prendre en charge les recherche avancée**
  
1. Définir une propriété pour chacun de vos critères de recherche.
    
2. Dans la section de code de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) méthode votre conteneur qui gère la propriété **PR_SEARCH** : 
    
1. Vérifiez que le client demande l’interface **IMAPIContainer** . Si une interface inappropriée est demandée, échouer et retourner MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Créer un nouvel objet de recherche qui prend en charge l’interface **IMAPIContainer** . 
    
3. À ce stade, un appel seront à la méthode **IMAPIProp::OpenProperty** de votre conteneur recherche pour extraire sa propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). Votre fournisseur doit fournir un affichage tableau, généralement par le biais d’un appel à [BuildDisplayTable](builddisplaytable.md), qui décrit la boîte de dialogue Recherche avancée du conteneur.
    
4. MAPI affiche la boîte de dialogue de recherche permettant à l’utilisateur d’entrer les critères appropriés. Lorsque l’utilisateur a terminé, MAPI appelle la méthode de [IMAPIProp::SetProps](imapiprop-setprops.md) du conteneur pour stocker les critères de recherche. 
    
5. Un appel est effectué à la demande de table des matières du conteneur de votre recherche. Renseignent la table des matières avec toutes les entrées dans le conteneur qui correspondent aux critères.
    

