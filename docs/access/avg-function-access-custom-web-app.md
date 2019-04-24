---
title: Fonction Avg (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcule la moyenne arithmétique d'un ensemble de valeurs contenues dans un champ spécifié.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282333"
---
# <a name="avg-function-access-custom-web-app"></a>Fonction Avg (application Web personnalisée Access)

Calcule la moyenne arithmétique d'un ensemble de valeurs contenues dans un champ spécifié.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **AVG (moy** ) (*NumericExpression*) 
  
La fonction **AVG** contient l'argument suivant. 
  
|**Argument**|**Description**|
|:-----|:-----|
|NumericExpression  <br/> |Expression de chaîne identifiant le champ qui contient les données numériques dont vous souhaitez calculer la moyenne ou une expression qui effectue un calcul à l'aide des données de ce champ. Les opérandes dans *NumericExpression* peuvent inclure le nom d'un champ de table, une variable ou une fonction (qui peut être intrinsèque ou définie par l'utilisateur, mais pas une des autres fonctions d'agrégation SQL).  <br/> |
   
## <a name="remarks"></a>Remarques

La moyenne calculée par **Avg** est la moyenne arithmétique (la somme des valeurs divisée par le nombre de valeurs). Vous pouvez utilisez **Avg**, par exemple, pour calculer des frais de port moyens. 
  
La fonction **AVG** n'inclut pas de valeurs **null** dans le calcul. 
  

