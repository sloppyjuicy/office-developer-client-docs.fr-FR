---
title: Mise en œuvre de la recherche avancée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 20282c78f6ff9003221429046fa9126cc4abaeec
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610467"
---
# <a name="implementing-advanced-searching"></a>Mise en œuvre de la recherche avancée

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains conteneurs de carnet d’adresses peuvent prendre en charge une fonctionnalité de recherche avancée qui permet aux clients d’effectuer des recherches sur des propriétés autres que **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Pour prendre en charge les recherches avancées, votre fournisseur doit implémenter un conteneur spécial accessible via la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) de vos autres conteneurs. **PR_SEARCH** contient un objet conteneur qui donne accès à un tableau d’affichage qui décrit la boîte de dialogue utilisée pour entrer et modifier les critères de recherche avancée. 
  
 **Pour prendre en charge la recherche avancée**
  
1. Définissez une propriété pour chacun de vos critères de recherche.
    
2. Dans la section de code de la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de votre conteneur qui gère la **propriété PR_SEARCH:** 
    
1. Vérifiez que le client demande l’interface **IMAPIContainer.** Si une interface inappropriée est demandée, échouez et renvoyez MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Créez un objet de recherche qui prend en charge l’interface **IMAPIContainer.** 
    
3. À ce stade, un appel est effectué à la méthode **IMAPIProp::OpenProperty** de votre conteneur de recherche pour récupérer sa propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). Votre fournisseur doit fournir une table d’affichage, généralement via un appel à [BuildDisplayTable](builddisplaytable.md), qui décrit la boîte de dialogue de recherche avancée du conteneur.
    
4. MAPI affiche la boîte de dialogue de recherche, ce qui permet à l’utilisateur d’entrer les critères appropriés. Lorsque l’utilisateur a terminé, MAPI appelle la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) du conteneur pour stocker les critères de recherche. 
    
5. Un appel est effectué pour demander la table des matières de votre conteneur de recherche. Remplir la table des matières avec toutes les entrées du conteneur qui correspondent aux critères.
    

