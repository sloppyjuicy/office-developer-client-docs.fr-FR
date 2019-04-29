---
title: Structure de flux PackedAnsiString
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ada86f04-e81b-4f97-b9c1-1c8ec5e1a5dd
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3e48e57deba5c274982eeb515d27f203ec5ac7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404504"
---
# <a name="packedansistring-stream-structure"></a>Structure de flux PackedAnsiString

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La structure de flux PackedAnsiString contient une représentation ANSI d'une chaîne, basée sur la page de code ANSI de l'ordinateur sur lequel Microsoft Outlook est en cours d'exécution. Cette chaîne n'est pas terminée par un caractère null. Les éléments de données dans ce flux sont stockés dans l'ordre d'octet Little-endian, immédiatement suivant l'ordre indiqué ci-dessous. Les éléments de données réels qui existent dépendent de la longueur de la chaîne en représentation ANSI.
  
- Pour une chaîne dont la représentation ANSI contient moins de 255 octets, les éléments de données sont les suivants:
    
  - Length: octet (1 octet), longueur, en nombre d'octets, de la représentation ANSI de la chaîne.
    
  - Caractères: tableau de CHAR. Le décompte de ce tableau est égal à l'élément de données length. Les données dans le tableau sont la représentation ANSI de la chaîne.
    
- Pour une chaîne dont la représentation ANSI contient 255 à 65535 octets, les éléments de données sont les suivants:
    
  - PréFixe: octet (1 octet), valeur de 255 (0xFF).
    
  - Length: WORD (2 octets), longueur, en nombre d'octets, de la représentation ANSI de la chaîne.
    
  - Caractères: tableau de CHAR. Le décompte de ce tableau est égal à l'élément de données length. Les données dans le tableau sont la représentation ANSI de la chaîne.
    
## <a name="see-also"></a>Voir aussi



[Éléments et champs Outlook](outlook-items-and-fields.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)

