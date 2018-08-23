---
title: Structure de flux SkipBlock
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2499587b-2a0e-4987-9bf7-591bef41b894
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b7be498473ef86b11006702f85089f0f95bb2e37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580900"
---
# <a name="skipblock-stream-structure"></a>Structure de flux SkipBlock

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une structure de flux SkipBlock est un bloc de données qui commence par un entier qui spécifie la longueur de la partie restante du bloc. Cette structure de flux de données existe dans un flux [FieldDefinition](fielddefinition-stream-structure.md) si la définition de champ est au format PropDefV2. 
  
L’objectif d’une structure de flux SkipBlock dépend de son emplacement relatif dans une série de comme les structures dans l’élément de données SkipBlocks d’un flux FieldDefinition. La série SkipBlocks doit contenir au moins une structure SkipBlock qui met fin à la série et comporte l’élément de données de taille égale à 0. Si la première structure n’est pas la structure de fin (autrement dit, l’élément de données de taille est supérieure à 0), Outlook suppose que la première structure Spécifie le nom de champ en Unicode (UTF-16).
  
Éléments de données dans ce flux de données sont stockés dans l’ordre de primauté des octets, immédiatement après l’autre dans l’ordre indiqué ci-dessous.
  
- Taille : DWORD (4 octets), la taille, en octets, de l’élément de données de contenu.
    
- Contenu : Un tableau d’octets. Le nombre de ce tableau est égal à l’élément de données de taille. La signification de l’élément de données de contenu dépend de l’emplacement de la structure SkipBlock dans la série et la version d’Outlook. Si la première structure SkipBlock n’est pas la structure rencontrée, Outlook considère que la première structure SkipBlock que la structure de flux [FirstSkipBlockContent](firstskipblockcontent-stream-structure.md) qui spécifie le nom de champ en Unicode. 
    
## <a name="see-also"></a>Voir aussi



[Champs et éléments Outlook](outlook-items-and-fields.md)
  
[Structures de flux](stream-structures.md)
  
[Structure de flux FieldDefinition](fielddefinition-stream-structure.md)
  
[Structure de flux FirstSkipBlockContent](firstskipblockcontent-stream-structure.md)

