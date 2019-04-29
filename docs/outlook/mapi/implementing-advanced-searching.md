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
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407388"
---
# <a name="implementing-advanced-searching"></a>Implémentation de la recherche avancée

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains conteneurs de carnet d'adresses prennent en charge une fonctionnalité de recherche avancée qui permet aux clients d'effectuer des recherches sur des propriétés autres que **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Pour prendre en charge les recherches avancées, votre fournisseur doit implémenter un conteneur spécial qui est accessible via la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de vos autres conteneurs. **PR_SEARCH** contient un objet Container qui fournit l'accès à une table d'affichage qui décrit la boîte de dialogue utilisée pour entrer et modifier les critères de recherche avancée. 
  
 **Pour prendre en charge la recherche avancée**
  
1. Définissez une propriété pour chacun de vos critères de recherche.
    
2. Dans la section de code de la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) de votre conteneur, qui gère la propriété **PR_SEARCH** : 
    
1. Vérifiez que le client demande l'interface **IMAPIContainer** . Si une interface inappropriée est demandée, échoue et renvoie MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Créer un objet de recherche qui prend en charge l'interface **IMAPIContainer** . 
    
3. À ce stade, un appel est effectué à la méthode **IMAPIProp:: OpenProperty** de votre conteneur de recherche pour récupérer sa propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). Votre fournisseur doit fournir une table d'affichage, généralement via un appel à [BuildDisplayTable](builddisplaytable.md), qui décrit la boîte de dialogue Recherche avancée du conteneur.
    
4. MAPI affiche la boîte de dialogue de recherche, qui permet à l'utilisateur d'entrer les critères appropriés. Une fois que l'utilisateur a terminé, MAPI appelle la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) du conteneur pour stocker les critères de recherche. 
    
5. Un appel sera effectué pour demander la table des matières de votre conteneur de recherche. Remplissez la table des matières avec toutes les entrées dans le conteneur qui correspondent aux critères.
    

