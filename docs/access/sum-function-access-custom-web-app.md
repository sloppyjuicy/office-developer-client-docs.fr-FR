---
title: SUM, fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Renvoie la somme de toutes les valeurs dans l’expression.
ms.openlocfilehash: 98531a0487505c24ed62034b7c283b9765a3e7a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781996"
---
# <a name="sum-function-access-custom-web-app"></a>SUM, fonction (accès personnalisé web app)

Renvoie la somme de toutes les valeurs dans l’expression.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Somme** (*NumericExpression*) 
  
La fonction **somme** contient l’argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *NumericExpression*  <br/> |Expression identifiant le champ qui contient les données numériques que vous souhaitez ajouter ou une expression qui effectue un calcul à l’aide des données dans ce champ. Les opérandes dans *NumericExpression* peuvent inclure le nom d’un champ de table, une constante ou une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas une des autres fonctions d’agrégation SQL).  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction **Sum** ignore les enregistrements qui contiennent des valeurs Null. 
  
La fonction **somme** peut uniquement être utilisée avec des colonnes numériques. 
  

