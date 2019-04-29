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
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415046"
---
# <a name="copying-mapi-properties"></a>Copie des propriétés MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients et les fournisseurs de services peuvent copier une ou plusieurs des propriétés d'un objet à l'aide des méthodes **IMAPIProp** et des fonctions d'API suivantes: 
  
- La méthode [IMAPIProp:: CopyTo](imapiprop-copyto.md) copie toutes les propriétés d'un objet vers un autre objet, éventuellement en excluant les propriétés sélectionnées. **CopyTo** est utilisé pour copier ou déménager n'importe quel type d'objet. 
    
- La méthode [IMAPIProp:: CopyProps](imapiprop-copyprops.md) copie les propriétés sélectionnées d'un objet. **CopyProps** est utilisé principalement avec les messages. Lorsqu'un client crée une copie transférée d'un message ou d'une réponse, **CopyProps** gère la copie des propriétés appropriées à partir du message d'origine. 
    
- La fonction [PropCopyMore](propcopymore.md) copie une valeur de propriété unique d'un emplacement vers un autre. Utilisez **PropCopyMore** avec précaution. Il est possible, lors de la copie d'une valeur à la fois, d'allouer de nombreux petits blocs de mémoire et de fragmenter la mémoire. 
    
- La fonction [ScCopyProps](sccopyprops.md) copie les valeurs des propriétés en bloc. **ScCopyProps** peut copier des valeurs de propriété qui ont été générées à partir de blocs de mémoire disjoints. Elle renvoie un nouveau tableau de propriétés. 
    
- Si le tableau de propriétés renvoyé par **ScCopyProps** doit être stocké sur le disque, utilisez la fonction [ScRelocProps](screlocprops.md) pour ajuster les pointeurs. **ScRelocProps** doit être appelé deux fois; une fois pour ajuster les adresses avant d'écrire l'opération de données, puis de nouveau lors de l'opération de lecture. La fonction **ScRelocProps** suppose que le tableau de valeurs de propriété a été alloué à l'origine dans une allocation unique. 
    
Les fonctions de l'API décrites dans la liste précédente copient les propriétés en mémoire plutôt que d'un objet à un autre. Ces fonctions sont actuellement prises en charge, mais elles ne sont pas prises en charge dans une version ultérieure.
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

