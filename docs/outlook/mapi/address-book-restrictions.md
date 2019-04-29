---
title: Restrictions du carnet d'adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432799"
---
# <a name="address-book-restrictions"></a>Restrictions du carnet d'adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnets d'adresses sont requis pour prendre en charge trois types de restrictions sur les tables de contenu de leurs conteneurs:
  
- Restrictions de propriété de nom ambigu
    
- Restrictions de propriété de clé d'instance
    
- Restrictions de contenu de nom d'affichage préfixé
    
Les restrictions de nom ambigus sont des restrictions de propriété utilisant la propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) pour faire correspondre les noms des destinataires aux entrées dans les conteneurs du carnet d'adresses. La restriction de propriété **PR_ANR** est un type de recherche qui permet aux fournisseurs de carnet d'adresses de choisir la propriété correspondante la mieux adaptée à leur conteneur. Par exemple, un fournisseur de carnet d'adresses peut implémenter la restriction **PR_ANR** en faisant correspondre les noms des destinataires à la propriété **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de chaque entrée de conteneur tandis qu'un autre fournisseur peut utiliser **PR_DISPLAY _NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
MAPI recommande que les implémentations de la restriction **PR_ANR** soient équilibrées entre les performances et la satisfaction des utilisateurs. La satisfaction des utilisateurs peut être compromise quand un fournisseur de carnet d'adresses implémente la restriction de telle sorte qu'il n'existe pas trop peu ou trop de correspondances. Certains fournisseurs de carnets d'adresses prennent en charge ce qui est connu sous le nom de nom unique ou courant qui n'est pas affichable dans une boîte de dialogue, mais peut correspondre à une restriction de nom ambigu. 
  
Une implémentation classique peut consister à analyser le nom d'affichage du destinataire en mots, ce qui correspond à n'importe quelle entrée contenant tous les mots. Attention aux détails, tels que la sensibilité de la position de Word, la correspondance entre les mots non consécutifs et le choix des caractères de séparation. Par exemple, si le nom à résoudre est «Bill L», une restriction **PR_ANR** classique sélectionnera les entrées suivantes, comme suit: 
  
- Billy Larson
    
- Bill Lee
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
Les restrictions de clé d'instance, ou **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), sont utilisées dans l'implémentation des zones de liste utilisées dans les applications clientes pour l'affichage des tables MAPI. Certaines implémentations de zone de liste permettent aux utilisateurs de sélectionner plusieurs sélections, de faire défiler vers le haut ou vers le bas et de revenir au premier élément sélectionné. Pour implémenter ce comportement, les clients appellent [IMAPITable:: FindRow](imapitable-findrow.md), en transmettant une restriction de propriété sur la propriété **PR_INSTANCE_KEY** à la méthode. Les fournisseurs de carnets d'adresses sont requis pour prendre en charge cette restriction. 
  
Une autre fonctionnalité des zones de liste utilisées pour l'affichage des tableaux est la possibilité de positionner le curseur en fonction d'un ensemble de caractères de préfixe. Lorsque l'utilisateur commence à taper des caractères de préfixe, le client place le curseur sur le premier élément qui commence par ces caractères. Les clients implémentent cette fonctionnalité avec une restriction de contenu basée sur la propriété **PR_DISPLAY_NAME** et le niveau de fuzzing FL_PREFIX. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

