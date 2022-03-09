---
title: Copie des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
ms.openlocfilehash: d9a1c2c8e37e0644cd0232f16ba6ee0b84c82247
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382201"
---
# <a name="copying-mapi-properties"></a>Copie des propriétés MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients et les fournisseurs de services peuvent copier une ou plusieurs propriétés d’un objet avec les méthodes et fonctions API **IMAPIProp** suivantes : 
  
- La [méthode IMAPIProp::CopyTo](imapiprop-copyto.md) copie toutes les propriétés d’un objet dans un autre objet, en excluant éventuellement les propriétés sélectionnées. **CopyTo** est utilisé pour copier ou déplacer n’importe quel type d’objet. 
    
- La [méthode IMAPIProp::CopyProps](imapiprop-copyprops.md) copie les propriétés sélectionnées d’un objet. **CopyProps est** utilisé principalement avec les messages. Lorsqu’un client crée une copie avancée d’un message ou d’une réponse, **CopyProps** gère la copie des propriétés appropriées à partir du message d’origine. 
    
- La [fonction PropCopyMore](propcopymore.md) copie une valeur de propriété unique d’un emplacement à un autre. Utilisez **PropCopyMore avec** précaution. Il est possible, lors de la copie d’une valeur à la fois, d’allouer de nombreux petits blocs de mémoire et de fragmenter la mémoire. 
    
- La [fonction ScCopyProps](sccopyprops.md) copie les valeurs des propriétés en bloc. **ScCopyProps peut** copier les valeurs de propriétés qui ont été construites à partir de blocs de mémoire disjoints. Elle renvoie un nouveau tableau de propriétés. 
    
- Si le tableau de propriétés renvoyé par **ScCopyProps** doit être stocké sur le disque, utilisez la [fonction ScRelocProps](screlocprops.md) pour ajuster les pointeurs. **ScRelocProps** doit être appelé deux fois ; une fois pour ajuster les adresses avant d’écrire l’opération de données, puis à nouveau pendant l’opération de lecture. La **fonction ScRelocProps** suppose que le tableau de valeurs de propriétés a été initialement alloué dans une allocation unique. 
    
Les fonctions d’API décrites dans la liste précédente copient les propriétés en mémoire plutôt que d’un objet à un autre. Ces fonctions sont actuellement pris en charge, mais peuvent ne pas l’être dans une version ultérieure.
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

