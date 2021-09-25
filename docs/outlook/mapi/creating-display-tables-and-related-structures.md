---
title: Création des tables d’affichage et des structures associées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 853a8db028d0e902f785cc3198e7994404af3ef1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592675"
---
# <a name="creating-display-tables-and-related-structures"></a>Création des tables d’affichage et des structures associées
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La création d’un tableau d’affichage est similaire à l’écriture d’un programme avec un langage de script. Vous pouvez créer un tableau d’affichage en appelant [BuildDisplayTable](builddisplaytable.md) ou en écrivant du code personnalisé pour remplir les lignes et les colonnes du tableau. En règle générale, vous devez utiliser la technique **BuildDisplayTable,** car elle est plus simple. 
  
Avant de pouvoir appeler **BuildDisplayTable** pour demander à MAPI de créer une table d’affichage, vous devez créer une hiérarchie de structures. La structure de niveau supérieur, [DTPAGE](dtpage.md), décrit une page de propriétés à onglets unique. Dans chaque structure **DTPAGE** se trouve une structure [DTCTL](dtctl.md) qui décrit un contrôle unique, tel qu’une zone d’édition ou une case d’option. Chaque **structure DTCTL** contient une structure spécifique au type de contrôle. Par exemple, si la structure **DTCTL** décrit un contrôle de zone d’édition, elle contient une structure **DTBLEDIT.** La structure **DTCTL d’une** bouton d’option contient une structure **DTBLRADIOBUTTON.** 
  
Ces structures sont directement liées **à BuildDisplayTable**; elles n’ont aucune signification en dehors du contexte de cette fonction. Lorsque vous appelez **BuildDisplayTable,** vous passez une ou plusieurs structures **DTPAGE** en tant que paramètres d’entrée. Les structures **DTPAGE** contiennent un tableau de structures **DTCTL** et un décompte du nombre de structures **DTCTL** dans le tableau. Il existe une structure pour chaque contrôle à afficher dans la boîte de dialogue. Les structures **DTPAGE** ont également une chaîne de caractères qui représente le nom d’un fichier d’aide et d’une ressource de boîte de dialogue correspondants. 
  
Chaque structure **DTCTL** d’une structure **DTPAGE** contient les données suivantes qui sont utilisées pour définir les propriétés du contrôle : 
  
- Type de contrôle pour **la** PR_CONTROL_TYPE ([PidTagControlType](pidtagcontroltype-canonical-property.md)).
    
- Indicateurs de contrôle pour la **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
    
- Données de notification pour la **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).
    
- Structure de contrôle pour la définition **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).
    
Les structures **DTCTL** contiennent également un identificateur de ressource et, pour les contrôles de zone de liste modifiable et de modification, un filtre de caractères. 
  
Le membre de structure de contrôle d’une structure **DTCTL** décrit les données uniques pour le type de contrôle. MAPI définit une structure différente pour chaque type de contrôle. Par exemple, les données d’un contrôle d’édition sont représentées par une structure **DTBLEDIT** ; Les données d’une zone de liste sont représentées par une structure **DTBLLBX.** 
  
La relation entre les trois types de structures de tableau d’affichage est indiquée dans l’illustration suivante. La boîte de dialogue décrite par ce tableau d’affichage possède deux contrôles : une étiquette et un contrôle d’édition. La structure **DTBLLBX** possède un membre de décalage d’étiquette, comme plusieurs structures de contrôle, qui décrit l’endroit où commence la chaîne de caractères de l’étiquette. Les chaînes de caractères d’étiquette sont généralement placées en mémoire immédiatement après la structure. 
  
**Structures de table d’affichage**
  
![Structures de table d’affichage](media/dtstruct.gif "Structures de table d’affichage")
  
## <a name="see-also"></a>Voir aussi

- [Implémentation d’une table d’affichage](display-table-implementation.md)

