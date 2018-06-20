---
title: Structure de flux PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5494558db65e19891848264c170ba85a55c5df71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784953"
---
# <a name="packedansistring-stream-structure"></a>Structure de flux PackedAnsiString

  
  
**S’applique à**: Outlook 
  
La structure de flux PackedAnsiString contient une représentation ANSI d’une chaîne, en fonction de la page de codes ANSI de l’ordinateur sur lequel Microsoft Outlook est en cours d’exécution. Cette chaîne n’est pas terminée par un caractère null. Éléments de données dans ce flux de données sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre indiqué ci-dessous. Les éléments de données réelles qui existent dépendent de la longueur de la chaîne de représentation ANSI.
  
- Une chaîne dont la représentation ANSI contient moins de 255 octets, les éléments de données sont les suivantes :
    
  - Durée : Octets (1 octet), la longueur, en octets, de la représentation de la chaîne ANSI.
    
  - Caractères : Un tableau de CHAR. Le nombre de ce tableau est égal à l’élément de données de longueur. Les données dans le tableau sont la représentation de la chaîne ANSI.
    
- Une chaîne dont la représentation ANSI contient 255 et 65535 octets, les éléments de données sont les suivantes :
    
  - Préfixe : Octets (1 octet), la valeur 255 (0xff).
    
  - Durée : Mot (2 octets), la longueur, en octets, de la représentation de la chaîne ANSI.
    
  - Caractères : Un tableau de CHAR. Le nombre de ce tableau est égal à l’élément de données de longueur. Les données dans le tableau sont la représentation de la chaîne ANSI.
    
## <a name="see-also"></a>Voir aussi



[Les champs et les éléments outlook](outlook-items-and-fields.md)
  
[Structures de flux de données](stream-structures.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)

