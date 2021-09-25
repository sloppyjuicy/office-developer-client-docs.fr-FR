---
title: Fonction Concat (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Renvoie une chaîne qui est le résultat de la combinaison de deux ou plusieurs valeurs de chaîne.
ms.openlocfilehash: 76e303659ea72a244ad83e12342f00d12c23bf09
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573346"
---
# <a name="concat-function-access-custom-web-app"></a>Fonction Concat (application web personnalisée Access)

Renvoie une chaîne qui est le résultat de la combinaison de deux ou plusieurs valeurs de chaîne.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**Concat** (*Valeur1*, *Valeur2*, ... [*ValueN*]) 
  
La **fonction Concat** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
|Valeur  <br/> |Valeur de chaîne à concaténer aux autres valeurs.  <br/> |
   
## <a name="remarks"></a>Remarques

**Concat** prend un nombre variable d’arguments de chaîne et les concatène en une seule chaîne. Un minimum de deux arguments de chaîne est requis ; Dans le cas contraire, une erreur est produite. 
  
Tous les arguments sont implicitement convertis en types de données de chaîne, puis concatés.
  
## <a name="example"></a>Exemple

L’expression suivante peut être utilisée pour afficher le nom complet d’une personne où la table contient les champs FirstName, MiddleInitial et LastName. Si le champ MiddleInitial est vide, seuls les champs FirstName et LastName sont combinés pour afficher le nom complet.
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


