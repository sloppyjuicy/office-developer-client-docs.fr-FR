---
title: Création d’afficher des tables et des structures associées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a8548040-13ed-4a9f-a7ca-de610f94d7df
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e17306e2b90f26dcef0a0214e78080fe78752e5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568566"
---
# <a name="creating-display-tables-and-related-structures"></a>Création d’afficher des tables et des structures associées
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Création d’un tableau de l’affichage est semblable à l’écriture d’un programme avec un langage de script. Vous pouvez créer un tableau d’affichage en appelant [BuildDisplayTable](builddisplaytable.md) ou écrire du code personnalisé pour remplir les lignes et colonnes de la table. En règle générale, vous devez utiliser la technique **BuildDisplayTable** , car il est plus simple. 
  
Avant de pouvoir appeler **BuildDisplayTable** pour demander MAPI pour créer une table d’affichage, il existe une hiérarchie de structures qui doit être généré. La structure de niveau supérieur, [DTPAGE](dtpage.md), décrit une page de propriétés à onglets unique. Dans chaque **DTPAGE** structure est une structure [DTCTL](dtctl.md) qui décrit une seule commande, comme une zone d’édition ou un bouton d’option. Chaque structure **DTCTL** contient une structure qui est spécifique au type de contrôle. Par exemple, si la structure **DTCTL** décrit un contrôle de zone de modification, il contient une structure **DTBLEDIT** . La structure **DTCTL** pour un bouton d’option contient une structure **DTBLRADIOBUTTON** . 
  
Ces structures sont directement associées à **BuildDisplayTable**; ils n’ont aucune signification en dehors du contexte de cette fonction. Lorsque vous appelez **BuildDisplayTable**, vous passez une ou plusieurs structures **DTPAGE** comme paramètres d’entrée. Les structures **DTPAGE** contiennent un tableau de structures **DTCTL** et le nombre de structures **DTCTL** dans le tableau. Il existe une structure pour chaque contrôle à afficher dans la boîte de dialogue. Structures **DTPAGE** ont également une chaîne de caractères qui représente le nom d’une aide fichier et la boîte de dialogue zone ressource correspondante. 
  
Chaque structure **DTCTL** dans une structure **DTPAGE** contient les données suivantes qui sont utilisées pour définir les propriétés du contrôle : 
  
- Le type de contrôle pour la définition de **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)).
    
- Indicateurs de contrôle pour la définition de **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)).
    
- Données de notification pour la définition de **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)).
    
- La structure de contrôle pour la définition de **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)).
    
Structures **DTCTL** également contenant un identificateur de ressource et, pour modifier et contrôles de zone de liste modifiable, un filtre de caractères. 
  
Le membre de structure de contrôle d’une structure **DTCTL** décrit les données qui sont uniques pour le type de contrôle. MAPI définit une structure différente pour chaque type de contrôle. Par exemple, les données d’un contrôle d’édition sont représentées par une structure **DTBLEDIT** ; les données d’une zone de liste sont représentées par une structure **DTBLLBX** . 
  
La relation entre les trois types de structures de table complet est indiquée dans l’illustration suivante. La boîte de dialogue décrite par cet affichage de la table a deux contrôles : un label et un contrôle d’édition. La structure **DTBLLBX** possède un membre de décalage de l’étiquette, comme plusieurs des structures de contrôle qui décrit où commence la chaîne de caractères pour l’étiquette. Étiquette des chaînes de caractères sont généralement placées en mémoire qui suit immédiatement la structure. 
  
**Structures de table d’affichage**
  
![Structures de table complet] (media/dtstruct.gif "Structures de table complet")
  
## <a name="see-also"></a>Voir aussi

- [Affichage tableau implémentation](display-table-implementation.md)

