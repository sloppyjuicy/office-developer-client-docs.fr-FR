---
title: Génération et utilisation d’identificateurs d’entrées dans les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 005742eaaba81600be249d52e5d8098e9f286f17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299810"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Génération et utilisation d’identificateurs d’entrées dans les fournisseurs de banques de messages

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu'un nouveau dossier ou message est créé dans une banque de messages, le fournisseur de banque de messages doit affecter cet objet à un identificateur d'entrée afin que les applications clientes puissent y faire référence. Les fournisseurs de banques de messages peuvent réutiliser les identificateurs d'entrée à long terme obsolètes des objets supprimés ou créer des identificateurs. Il n'y a pas d'exigence d'une façon ou d'une autre pour les fournisseurs de banque de messages; Toutefois, si cela est possible, un fournisseur de banque de messages doit toujours générer de nouveaux identificateurs d'entrée à long terme pour les nouveaux objets au lieu de réutiliser les anciens. Il convient de réutiliser des identificateurs d'entrée à court terme lorsque les objets auxquels ils font référence sont supprimés.
  
La raison de cette suppression est que les clients peuvent mettre en cache des identificateurs d'entrée, parfois pendant de longues périodes. Si cela se produit et que le fournisseur de banque de messages réutilise des identificateurs d'entrée, il est possible que l'identificateur d'entrée fasse référence à un autre objet lorsque le client ouvre l'identificateur d'entrée plutôt que lors de la première obtention de l'identificateur d'entrée. Si le fournisseur de banque de messages ne réutilise pas les identificateurs d'entrée ou utilise au moins le schéma de génération de l'identificateur d'entrée qui n'est pas répété longtemps, ce problème ne peut pas se produire.
  
De même, les fournisseurs de banques de messages doivent tenter de conserver les identificateurs d'entrée pour les dossiers et les messages lorsqu'ils sont déplacés dans la Banque de messages. Si le fournisseur de banque de messages peut effectuer cette opération, les références aux objets dans le magasin ne deviennent pas valides lorsque l'objet est déplacé vers un autre emplacement du magasin.
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnalit�s de la banque de messages](message-store-features.md)

