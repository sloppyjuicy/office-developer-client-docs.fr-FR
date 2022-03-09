---
title: Restrictions du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
ms.openlocfilehash: eea93c40f4172eddf5c5be2b13b08428291de5c7
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374536"
---
# <a name="address-book-restrictions"></a>Restrictions du carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnets d’adresses sont requis pour prendre en charge trois types de restrictions sur les tables de contenu de leurs conteneurs :
  
- Restrictions de propriété de nom ambigu
    
- Restrictions de propriété clé d’instance
    
- Restrictions de contenu de nom d’affichage préfixées
    
Les restrictions de nom ambigu sont des restrictions de propriété qui utilisent **la propriété PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) pour faire correspondre les noms des destinataires aux entrées des conteneurs de carnet d’adresses. La restriction **PR_ANR** de propriété est un type de recherche de « meilleure estimation » qui permet aux fournisseurs de carnets d’adresses de choisir la propriété correspondante qui fonctionne le mieux pour leur conteneur. Par exemple, un fournisseur de carnet d’adresses peut implémenter la restriction **PR_ANR** en mettant en correspondance les noms des destinataires avec la propriété **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de chaque entrée de conteneur, tandis qu’un autre fournisseur peut utiliser **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
MAPI recommande que les implémentations de la restriction **PR_ANR** équilibrent entre performances adéquates et satisfaction de l’utilisateur. La satisfaction des utilisateurs peut être compromise lorsqu’un fournisseur de carnet d’adresses implémente la restriction de telle sorte qu’un nombre de correspondances trop petit ou trop élevé soit trouvé. Certains fournisseurs de carnets d’adresses peuvent prendre en charge ce qu’on appelle un nom commun ou un nom qui n’est pas affichable dans une boîte de dialogue, mais qui peut correspondre à une restriction de nom ambigu. 
  
Une implémentation classique peut être d’afficher le nom complet du destinataire en mots, en correspondant à toute entrée contenant tous les mots. Les détails tels que la sensibilité à la position du mot, la correspondance des mots non conconsecutifs et le choix des caractères de séparation peuvent varier. Par exemple, si le nom à résoudre est « Bill L », **une restriction PR_ANR** type sélectionne les entrées suivantes en tant que correspondance : 
  
- Billy Larson
    
- Bill Lee
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
Les restrictions de clé d’instance ou les restrictions de propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) sont utilisées dans l’implémentation des zones de liste utilisées dans les applications clientes pour afficher les tables MAPI. Certaines implémentations de zone de liste permettent aux utilisateurs d’effectuer plusieurs sélections, de faire défiler vers le haut ou vers le bas et de revenir au premier élément sélectionné. Pour implémenter ce comportement, les clients appellent [IMAPITable::FindRow](imapitable-findrow.md), en passant une restriction de propriété **PR_INSTANCE_KEY** propriété à la méthode. Les fournisseurs de carnet d’adresses sont requis pour prendre en charge cette restriction. 
  
Une autre fonctionnalité des zones de liste utilisées pour l’affichage de tableau est la possibilité de positionner le curseur en fonction d’un ensemble de caractères de préfixe. Lorsque l’utilisateur commence à taper des caractères de préfixe, le client déplace le curseur vers le premier élément qui commence par ces caractères. Les clients implémentent cette fonctionnalité avec une restriction de contenu basée sur **la propriété PR_DISPLAY_NAME** et le niveau FL_PREFIX données. 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

