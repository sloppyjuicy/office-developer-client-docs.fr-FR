---
title: Fournisseurs de magasin de génération et l’utilisation d’identificateurs d’entrée dans un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0c43546a-4788-4852-bc89-d6baa4f33c94
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 10634305130b0f465482cce025018d4929350513
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565451"
---
# <a name="generating-and-using-entry-identifiers-in-message-store-providers"></a>Fournisseurs de magasin de génération et l’utilisation d’identificateurs d’entrée dans un message

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsqu’un nouveau dossier ou un message est créé dans une banque de messages, le fournisseur de banque de message doit affecter à cet objet un identificateur d’entrée afin que les applications clientes peuvent faire. Fournisseurs de banque de message pouvant réutiliser les anciens identificateurs d’entrée à long terme d’objets supprimés ou créer de nouveaux identificateurs. Il y a aucun moyen d’une ou l’autre pour les fournisseurs de banque de messages ; Toutefois, s’il est possible, un fournisseur de magasin de message doit toujours générer nouveaux identificateurs d’entrée à long terme pour les nouveaux objets plutôt que d’anciens réutilisation. Il convient de réutiliser les identificateurs d’entrée à court terme lorsqu’ils se rapportent aux objets sont supprimés.
  
La raison de cette suppression est que les clients peuvent effectuer les identificateurs d’entrée, parfois pour de longues périodes. Si cela se produit et le fournisseur de banque de messages réutilise les identificateurs d’entrée, il est possible de l’identificateur d’entrée faire référence à un autre objet lorsque le client s’ouvre l’identificateur d’entrée que lorsqu’il obtenu tout d’abord l’identificateur d’entrée. Si le fournisseur de banque de messages ne réutilise pas les identificateurs d’entrée, ou au moins utilise un modèle génération identificateur d’entrée n’est pas extensible pour beaucoup de temps, ce problème ne peut pas se produire.
  
De même, les fournisseurs de magasins de message doivent essayer de conserver les identificateurs d’entrée pour les dossiers et messages lorsqu’ils sont déplacés dans la banque de messages. Si le fournisseur de banque de message peut faire que, les références à des objets dans le magasin ne prendra non valides lorsque l’objet est déplacé vers un autre emplacement dans le magasin.
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnalit�s de la banque de messages](message-store-features.md)

