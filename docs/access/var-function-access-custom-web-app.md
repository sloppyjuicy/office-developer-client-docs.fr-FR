---
title: Var Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Renvoie la variation statistique d’un échantillon de population représenté sous la mesure d’un ensemble de valeurs contenues dans un champ spécifié dans une requête.
ms.openlocfilehash: a6ce06ea74c32a52685d1debee14345b193920e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588391"
---
# <a name="var-function-access-custom-web-app"></a>Var Function (Access custom web app)

Renvoie la variation statistique d’un échantillon de population représenté sous la mesure d’un ensemble de valeurs contenues dans un champ spécifié dans une requête.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Var** (*NumericExpression*) 
  
La **fonction Var** contient l’argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *NumericExpression*  <br/> |Expression de texte identifiant le champ qui contient les données numériques à évaluer ou expression qui effectue un calcul à l’aide des données de ce champ. Les opérandes dans *NumericExpression* peuvent inclure le nom d’un champ de table, d’une constante ou d’une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas l’une des autres fonctions d’agrégation SQL).  <br/> |
   
## <a name="remarks"></a>Remarques

 **Var** ne peut être utilisé qu’avec des colonnes numériques. Les valeurs Null sont ignorées. 
  

