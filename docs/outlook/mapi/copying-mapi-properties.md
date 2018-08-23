---
title: Copie des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 556ea9faedf0d9a02b0cff1bb2f1750289cc4d1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565080"
---
# <a name="copying-mapi-properties"></a>Copie des propriétés MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Clients et fournisseurs de services peuvent copier une ou plusieurs des propriétés d’un objet avec les fonctions de l’API des méthodes **IMAPIProp** suivantes : 
  
- La méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) copie toutes les propriétés d’un objet à un autre objet, si vous le souhaitez à l’exception des propriétés sélectionnées. **CopyTo** est utilisé pour la copie ou le déplacement de n’importe quel type d’objet. 
    
- La méthode [IMAPIProp::CopyProps](imapiprop-copyprops.md) copie les propriétés sélectionnées d’un objet. **CopyProps** est utilisée principalement avec des messages. Lorsqu’un client crée une copie transférée d’un message ou d’une réponse, poignées **CopyProps** copie les propriétés appropriées à partir du message d’origine. 
    
- La fonction [PropCopyMore](propcopymore.md) copie une seule valeur de propriété d’un emplacement vers un autre. Utilisez **PropCopyMore** avec précaution. Il est possible, lors de la copie d’une valeur à la fois — pour allouer de nombreux petits blocs de mémoire et provoquer le fragment de mémoire. 
    
- La fonction [ScCopyProps](sccopyprops.md) copie les valeurs de propriété en bloc. **ScCopyProps** peut copier les valeurs de propriété qui ont été générés à partir des blocs de mémoire. Il retourne un nouveau tableau de propriété. 
    
- Si le tableau renvoyé par **ScCopyProps** de la propriété doit être stocké sur disque, utilisez la fonction [ScRelocProps](screlocprops.md) pour ajuster les pointeurs. **ScRelocProps** doit être appelée deux fois ; une fois pour ajuster les adresses avant d’écrire l’opération de données, puis à nouveau lors de l’opération de lecture. La fonction **ScRelocProps** suppose que le tableau de valeurs de propriété alloué initialement dans une affectation unique. 
    
Les fonctions API décrites dans les précédente liste Propriétés en mémoire, au lieu d’un objet à un autre objet. Ces fonctions sont actuellement pris en charge, mais ne peuvent pas pris en charge dans une version future.
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

