---
title: Création des tables d’affichage et des structures associées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 350272324c3827f4630f0cf35e3ade0ff213ac4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335611"
---
# <a name="creating-display-tables-and-related-structures"></a>Création des tables d’affichage et des structures associées
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La création d'une table d'affichage est semblable à l'écriture d'un programme à l'aide d'un langage de script. Vous pouvez créer une table d'affichage en appelant [BuildDisplayTable](builddisplaytable.md) ou en écrivant du code personnalisé pour remplir les lignes et les colonnes du tableau. En règle générale, vous devez utiliser la technique **BuildDisplayTable** , car elle est plus simple. 
  
Avant de pouvoir appeler **BuildDisplayTable** pour inviter MAPI à créer une table d'affichage, il existe une hiérarchie de structures que vous devez créer. La structure de niveau supérieur, [DTPAGE](dtpage.md), décrit une seule page de propriétés à onglets. Dans chaque structure **DTPAGE** est une structure [DTCTL](dtctl.md) qui décrit un seul contrôle, tel qu'une zone d'édition ou une case d'option. Chaque structure **DTCTL** contient une structure propre au type de contrôle. Par exemple, si la structure **DTCTL** décrit un contrôle de zone d'édition, elle contiendra une structure **DTBLEDIT** . La structure **DTCTL** d'une case d'option contient une structure **DTBLRADIOBUTTON** . 
  
Ces structures sont directement liées à **BuildDisplayTable**; elles n'ont aucune signification en dehors du contexte de cette fonction. Lorsque vous appelez **BuildDisplayTable**, vous transmettez une ou plusieurs structures **DTPAGE** en tant que paramètres d'entrée. Les structures **DTPAGE** contiennent un tableau de structures **DTCTL** et le nombre de structures **DTCTL** dans le tableau. Il existe une structure pour chaque contrôle à afficher dans la boîte de dialogue. Les structures **DTPAGE** ont également une chaîne de caractères qui représente le nom d'un fichier d'aide et d'une ressource de boîte de dialogue correspondants. 
  
Chaque structure **DTCTL** dans une structure **DTPAGE** contient les données suivantes qui sont utilisées pour définir les propriétés du contrôle: 
  
- Type de contrôle pour la définition de **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).
    
- Indicateurs de contrôle pour la définition de **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
    
- Données de notification pour le paramètre **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).
    
- La structure de contrôle pour la définition de **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).
    
Les structures **DTCTL** contiennent également un identificateur de ressource et, pour les contrôles de zone de liste modifiable et de modification, un filtre de caractères. 
  
Le membre de la structure de contrôle d'une structure **DTCTL** décrit les données propres au type de contrôle. MAPI définit une structure différente pour chaque type de contrôle. Par exemple, les données d'un contrôle d'édition sont représentées par une structure **DTBLEDIT** ; les données d'une zone de liste sont représentées par une structure **DTBLLBX** . 
  
La relation entre les trois types de structures de tables d'affichage est illustrée dans l'illustration suivante. La boîte de dialogue décrite par cette table d'affichage comporte deux contrôles: une étiquette et un contrôle d'édition. La structure **DTBLLBX** a un membre de décalage d'étiquette, comme effectuer plusieurs structures de contrôle, qui décrit l'emplacement où commence la chaîne de caractères de l'étiquette. Les chaînes de caractères d'étiquette sont généralement placées en mémoire immédiatement après la structure. 
  
**Structures de table d’affichage**
  
![Structures des tables d'affichage] (media/dtstruct.gif "Structures des tables d'affichage")
  
## <a name="see-also"></a>Voir aussi

- [Implémentation d’une table d’affichage](display-table-implementation.md)

