---
title: Fonction concat (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Renvoie une chaîne qui est le résultat de la combinaison de deux ou plusieurs valeurs de chaîne.
ms.openlocfilehash: fc0de43e5e42cc1c39ee89cf76058b8039daf279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781794"
---
# <a name="concat-function-access-custom-web-app"></a>Fonction concat (accès personnalisé web app)

Renvoie une chaîne qui est le résultat de la combinaison de deux ou plusieurs valeurs de chaîne.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**Concat** (*Valeur1*, *valeur2*... [*ValeurN*]) 
  
La fonction **Concat** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
|Valeur  <br/> |Valeur de chaîne concaténation sur les autres valeurs.  <br/> |
   
## <a name="remarks"></a>Remarques

**Concat** accepte un nombre variable d’arguments de chaîne et concaténé les dans une chaîne unique. Un minimum de deux arguments de chaîne sont nécessaires ; dans le cas contraire, une erreur est générée. 
  
Tous les arguments sont implicitement convertis en données de type chaîne et puis concaténées.
  
## <a name="example"></a>Exemple

L’expression suivante peut être utilisée pour afficher le nom complet d’une personne où la table contient les champs FirstName, MiddleInitial et LastName. Si le champ « MiddleInitial » est vide, seuls les champs FirstName et LastName sont combinés pour afficher le nom complet.
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


