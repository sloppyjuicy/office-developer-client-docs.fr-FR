---
title: Identificateurs d'entrée à long terme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409222"
---
# <a name="long-term-entry-identifiers"></a>Identificateurs d'entrée à long terme

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un identificateur d'entrée à long terme est affecté par un fournisseur de services à un objet lorsqu'un objet requiert un identificateur avec une durée de vie prolongée. Les identificateurs d'entrée à long terme sont toujours valides pendant des semaines ou des mois, et peuvent être valides sur d'autres stations de travail, selon le fournisseur. Les identificateurs à long terme créés par des fournisseurs de carnet d'adresses pour les destinataires personnalisés sont universellement valides. 
  
Les identificateurs d'entrée à long terme sont affectés à des banques de messages, des dossiers, des messages, des conteneurs de carnet d'adresses, des utilisateurs de messagerie et des listes de distribution. Lorsque les applications clientes appellent la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de ces objets, il s'agit toujours d'un identificateur d'entrée à long terme renvoyé. 
  
Les identificateurs d'entrée à long terme doivent être uniques dans toutes les banques de messages du profil actif; par conséquent, lorsqu'un message ou un dossier est copié d'une banque de messages à une autre, un nouvel identificateur d'entrée doit lui être attribué. Lorsqu'un objet de banque de messages est déplacé, le fournisseur de banque de messages qui implémente le déplacement détermine si l'identificateur d'entrée d'origine reste valide. Certains fournisseurs de services affectent de nouveaux identificateurs d'entrée aux objets déplacés; d'autres non. En cas de modification, le nouvel identificateur d'entrée est inclus dans les informations transmises aux clients lorsqu'ils sont avertis du déplacement. 
  
En règle générale, les fournisseurs de banque de messages implémentent le comportement suivant lorsqu'ils déplacent des dossiers:
  
- Lorsqu'un dossier est déplacé d'une banque de messages vers une autre pour un autre type, l'identificateur de l'entrée est garanti.
    
- Lorsqu'un dossier est déplacé d'une banque de messages vers une autre banque du même type, l'identificateur de l'entrée est presque toujours modifié.
    
- Lorsqu'un dossier est déplacé vers un autre emplacement dans le même magasin de messages, l'identificateur d'entrée peut être modifié ou non, selon le fournisseur de banque de messages.
    
Le fait de renommer un dossier sans modifier son dossier parent ne provoque généralement pas la modification de l'identificateur d'entrée. 
  
## <a name="see-also"></a>Voir aussi



[Identificateurs d'entrée MAPI](mapi-entry-identifiers.md)

