---
title: Fonction VAR (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Renvoie la variance pour un échantillon de population représenté par un ensemble de valeurs contenues dans un champ spécifié dans une requête.
ms.openlocfilehash: 9937f1985c0a7df5eb06977333ab889947891380
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782008"
---
# <a name="var-function-access-custom-web-app"></a>Fonction VAR (accès personnalisé web app)

Renvoie la variance pour un échantillon de population représenté par un ensemble de valeurs contenues dans un champ spécifié dans une requête.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Var** (*NumericExpression*) 
  
La fonction **Var** contient l’argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *NumericExpression*  <br/> |Une expression de texte identifiant le champ qui contient les données numériques à évaluer ou une expression qui effectue un calcul à l’aide des données dans ce champ. Les opérandes dans *NumericExpression* peuvent inclure le nom d’un champ de table, une constante ou une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas une des autres fonctions d’agrégation SQL).  <br/> |
   
## <a name="remarks"></a>Remarques

 **Var** peut être utilisé avec des colonnes numériques uniquement. Les valeurs nulles sont ignorées. 
  

