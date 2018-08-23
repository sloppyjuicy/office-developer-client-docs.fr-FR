---
title: Structure de flux PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 00791ab47cc3c6bd435d6f581e5ada53ae59d73b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569196"
---
# <a name="packedunicodestring-stream-structure"></a>Structure de flux PackedUnicodeString

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La structure de flux PackedUnicodeString contient une représentation Unicode (UTF-16) d’une chaîne. Cette chaîne n’est pas terminée par un caractère null. Éléments de données dans ce flux de données sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre indiqué ci-dessous. Les éléments de données réelles qui existent dépendent de la longueur de la chaîne de représentation UTF-16.
  
- Une chaîne dont la représentation UTF-16 contient moins de 255 WCHAR, les éléments de données sont les suivantes :
    
  - Durée : Octets (1 octet), la longueur, en nombre de WCHAR, de la représentation de la chaîne UTF-16.
    
  - Caractères : Tableau de WCHAR. Le nombre de ce tableau est égal à l’élément de données de longueur. Les données dans le tableau sont la représentation de la chaîne UTF-16.
    
- Une chaîne dont la représentation UTF-16 contient WCHAR 255 et 65535, les éléments de données sont les suivantes :
    
  - Préfixe : Octets (1 octet), la valeur 255 (0xff).
    
  - Durée : Mot (2 octets), la longueur, en nombre de WCHAR, de la représentation de la chaîne UTF-16.
    
  - Caractères : Tableau de WCHAR. Le nombre de ce tableau est égal à l’élément de données de longueur. Les données dans le tableau sont la représentation de la chaîne UTF-16.
    
## <a name="see-also"></a>Voir aussi



[Champs et éléments Outlook](outlook-items-and-fields.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)

