---
title: Identificateurs d’entrée à long terme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 589420db48edb348a22f34ce72b948f4d8207ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784535"
---
# <a name="long-term-entry-identifiers"></a>Identificateurs d’entrée à long terme

  
  
**S’applique à**: Outlook 
  
Un identificateur d’entrée à long terme est affecté par un fournisseur de services à un objet lorsqu’un objet nécessite un identificateur ayant une durée de vie prolongée. Identificateurs d’entrée à long terme sont toujours valables pour plusieurs semaines ou mois et peuvent être valides sur les autres stations de travail, selon le fournisseur. Les identificateurs à long terme créés par les fournisseurs de carnet d’adresses pour les destinataires personnalisés valent universel. 
  
Identificateurs d’entrée à long terme sont affectés à des banques de messages, les dossiers, messages, conteneurs de carnet d’adresses, messagerie utilisateurs et distribution listes. Les applications clientes d’appeler la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de ces objets, il est toujours un identificateur d’entrée à long terme qui est renvoyé. 
  
Identificateurs d’entrée à long terme doivent être uniques parmi toutes les banques de messages dans le profil actif ; Par conséquent, lorsqu’un message ou un dossier est copié à partir d’une banque d’informations à un autre, il doit être affecté un nouvel identificateur d’entrée. Lorsqu’un objet de banque de messages est déplacé, le fournisseur de banque de messages qui implémente le déplacement détermine si l’identificateur d’entrée d’origine reste valide. Certains fournisseurs de services attribuer de nouveaux identificateurs d’entrée aux objets déplacées ; d’autres ne le sont pas. S’il existe une modification, l’identificateur d’entrée sera inclus dans les informations transmises aux clients lorsqu’ils sont avertis du déplacement. 
  
En règle générale, les fournisseurs de magasins de message implémentent le comportement suivant lorsque le déplacement de dossiers :
  
- Lorsqu’un dossier est déplacé vers un autre magasin d’un type différent à partir d’une banque d’informations, l’identificateur d’entrée est garanti à modifier.
    
- Lorsqu’un dossier est déplacé vers un autre magasin du même type à partir d’une banque d’informations, l’identificateur d’entrée change presque toujours.
    
- Lorsqu’un dossier est déplacé vers un autre emplacement dans le même magasin de message, l’identificateur d’entrée peut-être ou ne peut pas changer, selon le fournisseur de banque de messages.
    
Renommer un dossier sans modifier son dossier parent généralement n’entraîne pas l’identificateur d’entrée à modifier. 
  
## <a name="see-also"></a>Voir aussi



[Identificateurs d’entrée MAPI](mapi-entry-identifiers.md)

