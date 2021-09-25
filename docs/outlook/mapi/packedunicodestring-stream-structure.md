---
title: Structure de flux PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 73a3f6f8ca3dd23326f28ea18228c09cf310d444
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625118"
---
# <a name="packedunicodestring-stream-structure"></a>Structure de flux PackedUnicodeString

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La structure de flux PackedUnicodeString contient une représentation Unicode (UTF-16) d’une chaîne. Cette chaîne n’est pas terminée par un caractère null. Les éléments de données de ce flux sont stockés dans l’ordre des petits bouts, immédiatement après les autres dans l’ordre indiqué ci-dessous. Les éléments de données réels qui existent dépendent de la longueur de la chaîne dans la représentation UTF-16.
  
- Pour une chaîne dont la représentation UTF-16 contient moins de 255 WCHAR, les éléments de données sont les suivants :
    
  - Longueur : BYTE (1 byte), longueur, en nombre de WCHAR, de la représentation UTF-16 de la chaîne.
    
  - Caractères : tableau de WCHAR. Le nombre de ce tableau est égal à l’élément de données Length. Les données du tableau sont la représentation UTF-16 de la chaîne.
    
- Pour une chaîne dont la représentation UTF-16 contient 255 à 65 535 WCHAR, les éléments de données sont les suivants :
    
  - Préfixe : BYTE (1 byte), la valeur de 255 (0xff).
    
  - Longueur : WORD (2 octets), longueur, en nombre de WCHAR, de la représentation UTF-16 de la chaîne.
    
  - Caractères : tableau de WCHAR. Le nombre de ce tableau est égal à l’élément de données Length. Les données du tableau sont la représentation UTF-16 de la chaîne.
    
## <a name="see-also"></a>Voir aussi



[Outlook Éléments et champs](outlook-items-and-fields.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)

