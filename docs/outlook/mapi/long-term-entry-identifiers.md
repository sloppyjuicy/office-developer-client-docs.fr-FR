---
title: Long-Term d’entrée de données
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
ms.openlocfilehash: b7791b3378ee96a3111ab1e6e9f6ee9e59078e33
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373416"
---
# <a name="long-term-entry-identifiers"></a>Long-Term d’entrée de données

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un identificateur d’entrée à long terme est attribué par un fournisseur de services à un objet lorsqu’un objet nécessite un identificateur dont la durée de vie est prolongée. Les identificateurs d’entrée à long terme sont toujours valides pendant des semaines ou des mois et peuvent être valides sur d’autres stations de travail, selon le fournisseur. Les identificateurs à long terme créés par les fournisseurs de carnets d’adresses pour les destinataires personnalisés sont universellement valides. 
  
Les identificateurs d’entrée à long terme sont affectés aux magasins de messages, aux dossiers, aux messages, aux conteneurs de carnet d’adresses, aux utilisateurs de messagerie et aux listes de distribution. Lorsque les applications clientes appellent la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de ces objets, il s’agit toujours d’un identificateur d’entrée à long terme qui est renvoyé. 
  
Les identificateurs d’entrée à long terme doivent être uniques dans toutes les magasins de messages du profil actif . par conséquent, lorsqu’un message ou un dossier est copié d’une magasin de messages vers une autre, un nouvel identificateur d’entrée doit lui être affecté. Lorsqu’un objet de la boutique de messages est déplacé, le fournisseur de magasins de messages qui implémente le déplacement détermine si l’identificateur d’entrée d’origine reste valide. Certains fournisseurs de services affectent de nouveaux identificateurs d’entrée aux objets déplacés ; d’autres non. En cas de modification, le nouvel identificateur d’entrée est inclus dans les informations transmises aux clients lorsqu’ils sont avertis du déplacement. 
  
En règle générale, les fournisseurs de magasins de messages implémentent le comportement suivant lorsqu’ils déplacent des dossiers :
  
- Lorsqu’un dossier est déplacé d’une magasin de messages vers une autre de type différent, il est garanti que l’identificateur d’entrée change.
    
- Lorsqu’un dossier est déplacé d’une magasin de messages vers une autre du même type, l’identificateur d’entrée change presque toujours.
    
- Lorsqu’un dossier est déplacé vers un autre emplacement au sein de la même magasin de messages, l’identificateur d’entrée peut changer ou non, selon le fournisseur de la boutique de messages.
    
En règle générale, le fait de renommer un dossier sans modifier son dossier parent n’entraîne pas la modification de l’identificateur d’entrée. 
  
## <a name="see-also"></a>Voir aussi



[Identificateurs d’entrée MAPI](mapi-entry-identifiers.md)

