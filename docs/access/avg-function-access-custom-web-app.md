---
title: Fonction AVG (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcule la moyenne arithmétique d’un ensemble de valeurs contenues dans un champ spécifié.
ms.openlocfilehash: afe832a51fc9cd3b224087a0b06fe539f6a7004b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781815"
---
# <a name="avg-function-access-custom-web-app"></a>Fonction AVG (accès personnalisé web app)

Calcule la moyenne arithmétique d’un ensemble de valeurs contenues dans un champ spécifié.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Avg** (*NumericExpression*) 
  
La fonction **Avg** contient l’argument suivant. 
  
|**Argument**|**Description**|
|:-----|:-----|
|NumericExpression  <br/> |Expression chaîne identifiant le champ qui contient les données numériques que vous voulez la moyenne ou une expression qui effectue un calcul à l’aide des données dans ce champ. Les opérandes dans *NumericExpression* peuvent inclure le nom d’un champ de table, une variable ou une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas une des autres fonctions d’agrégation SQL).  <br/> |
   
## <a name="remarks"></a>Remarques

La moyenne calculée par **Avg** est la moyenne arithmétique (somme des valeurs divisée par le nombre de valeurs). Vous pouvez utiliser **Avg**, par exemple, pour calculer la moyenne des frais. 
  
La fonction **Avg** n’inclut pas toutes les valeurs **Null** dans le calcul. 
  

