---
title: Structure de flux PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2b4dcdcb50fb04410ed93940b46ea7a0d74fff41
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784956"
---
# <a name="packedunicodestring-stream-structure"></a>Structure de flux PackedUnicodeString

  
  
**S’applique à**: Outlook 
  
La structure de flux PackedUnicodeString contient une représentation Unicode (UTF-16) d’une chaîne. Cette chaîne n’est pas terminée par un caractère null. Éléments de données dans ce flux de données sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre indiqué ci-dessous. Les éléments de données réelles qui existent dépendent de la longueur de la chaîne de représentation UTF-16.
  
- Une chaîne dont la représentation UTF-16 contient moins de 255 WCHAR, les éléments de données sont les suivantes :
    
  - Durée : Octets (1 octet), la longueur, en nombre de WCHAR, de la représentation de la chaîne UTF-16.
    
  - Caractères : Tableau de WCHAR. Le nombre de ce tableau est égal à l’élément de données de longueur. Les données dans le tableau sont la représentation de la chaîne UTF-16.
    
- Une chaîne dont la représentation UTF-16 contient WCHAR 255 et 65535, les éléments de données sont les suivantes :
    
  - Préfixe : Octets (1 octet), la valeur 255 (0xff).
    
  - Durée : Mot (2 octets), la longueur, en nombre de WCHAR, de la représentation de la chaîne UTF-16.
    
  - Caractères : Tableau de WCHAR. Le nombre de ce tableau est égal à l’élément de données de longueur. Les données dans le tableau sont la représentation de la chaîne UTF-16.
    
## <a name="see-also"></a>Voir aussi



[Les champs et les éléments outlook](outlook-items-and-fields.md)
  
[Structures de flux de données](stream-structures.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)

