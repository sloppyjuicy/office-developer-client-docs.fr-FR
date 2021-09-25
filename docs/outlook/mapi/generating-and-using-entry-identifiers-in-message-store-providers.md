---
title: Génération et utilisation d’identificateurs d’entrées dans les fournisseurs de banques de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6d5cc5899c911e3fbf9e47746d223ba6b5150130
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580201"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Génération et utilisation d’identificateurs d’entrées dans les fournisseurs de banques de messages

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un nouveau dossier ou message est créé dans une magasin de messages, le fournisseur de la boutique de messages doit affecter à cet objet un identificateur d’entrée afin que les applications clientes y font référence. Les fournisseurs de magasins de messages peuvent réutiliser les identificateurs d’entrée à long terme des objets supprimés ou créer de nouveaux identificateurs. Il n’existe aucune exigence d’une manière ou d’une autre pour les fournisseurs de magasins de messages ; toutefois, si possible, un fournisseur de magasins de messages doit toujours générer de nouveaux identificateurs d’entrée à long terme pour les nouveaux objets plutôt que de les réutiliser. Il est correct de réutiliser les identificateurs d’entrée à court terme lorsque les objets référents sont supprimés.
  
La raison de cette suppression est que les clients peuvent mettre en cache les identificateurs d’entrée, parfois pour de longues périodes. Si cela se produit et que le fournisseur de la boutique de messages réutilise les identificateurs d’entrée, il est possible pour l’identificateur d’entrée de faire référence à un autre objet lorsque le client ouvre l’identificateur d’entrée par rapport à la première fois qu’il a obtenu l’identificateur d’entrée. Si le fournisseur de la boutique de messages ne réutilise pas les identificateurs d’entrée ou utilise au moins un schéma de génération d’identificateur d’entrée qui ne se répète pas pendant très longtemps, ce problème ne peut pas se produire.
  
De même, les fournisseurs de magasins de messages doivent essayer de conserver les identificateurs d’entrée pour les dossiers et les messages lorsqu’ils sont déplacés dans la magasin de messages. Si le fournisseur de la boutique de messages peut le faire, les références aux objets de la boutique ne deviennent pas non valides lorsque l’objet est déplacé vers un autre emplacement de la boutique.
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnalit�s de la banque de messages](message-store-features.md)

