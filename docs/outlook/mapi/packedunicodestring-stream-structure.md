---
title: Structure de flux PackedUnicodeString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e4cb1613-7e81-432a-ae3a-7fedb05dac65
ms.openlocfilehash: 27f04f03f9271faf075c673a5ea8f167c97dc7ab
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63381991"
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



[Outlook et champs](outlook-items-and-fields.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)

