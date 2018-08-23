---
title: Restrictions de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 54cd90cac6c00e8cf274e0b78a1bfec32401bb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576511"
---
# <a name="address-book-restrictions"></a>Restrictions de carnet d’adresses

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournisseurs de carnet d’adresses sont requis pour prendre en charge trois types de restrictions sur les tables des matières de leurs conteneurs :
  
- Restrictions de propriété nom ambigu
    
- Restrictions de propriété de clé d’instance
    
- Restrictions de contenu de nom complet préfixé
    
Restrictions de nom ambigu sont des restrictions de propriété à l’aide de la propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) pour faire correspondre les noms des destinataires avec des entrées dans les conteneurs de carnet d’adresses. La restriction de propriété **PR_ANR** est un type « mieux deviner » de la recherche grâce à laquelle les fournisseurs de carnet d’adresses peuvent choisir la propriété correspondante qui convient le mieux pour leur conteneur. Par exemple, un fournisseur de carnet d’adresses peut implémenter la restriction **PR_ANR** par les noms des destinataires correspondants à la propriété **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) de chaque entrée de conteneur alors qu’un autre fournisseur peut utiliser **PR_DISPLAY _Ordinateur** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
MAPI recommande que les implémentations de la restriction **PR_ANR** un équilibre entre la satisfaction client et des performances optimales. Satisfaction des utilisateurs peut être compromise lorsqu’un fournisseur de carnet d’adresses implémente la restriction de telle sorte que trop ou trop peu de correspondance. Certains fournisseurs de carnet d’adresses prend en charge ce que l'on appelle un nom unique, ou courant, qui n’est pas affichable dans une boîte de dialogue, mais peut correspondre à une restriction de nom ambigu. 
  
Une implémentation typique peut être pour analyser le nom d’affichage du destinataire en mots, correspondant à une entrée qui contient tous les mots. Attention aux détails tels que la sensibilité à la position de word, si les mots non consécutifs sont filtrés et le choix des caractères de séparation peuvent varier. Par exemple, si le nom est résolu est « L Bill », une restriction **PR_ANR** par défaut, sélectionnez les entrées suivantes comme correspondants : 
  
- Billy Larson
    
- Bill Lee
    
- Offres d’emploi Logan Bill. 
    
- Sam Bill Lee
    
Restrictions clés instance ou des restrictions de propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), sont utilisées dans l’implémentation de zones de liste qui sont utilisés dans les applications clientes pour l’affichage des tables MAPI. Certaines implémentations de zone de liste Autoriser les utilisateurs à effectuer des sélections multiples, défiler vers le haut ou vers le bas et de retour sur le premier élément sélectionné. Pour implémenter ce comportement, les clients appellent [IMAPITable::FindRow](imapitable-findrow.md), en passant une restriction de propriété sur la propriété **PR_INSTANCE_KEY** à la méthode. Fournisseurs de carnet d’adresses sont requis pour prendre en charge cette restriction. 
  
Une autre fonctionnalité de zones de liste utilisé pour l’affichage tableau est la capacité pour placer le curseur basé sur un jeu de caractères de préfixe. Lorsque l’utilisateur commence à taper des caractères de préfixe, le client place le curseur sur le premier élément qui commence par ces caractères. Clients implémentent cette fonctionnalité avec une restriction de contenu en fonction de la propriété **PR_DISPLAY_NAME** et le niveau approximatif FL_PREFIX. 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

