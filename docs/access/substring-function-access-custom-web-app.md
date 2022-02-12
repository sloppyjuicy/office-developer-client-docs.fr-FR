---
title: SubString Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Renvoie une partie d’une expression de texte.
ms.openlocfilehash: 19a7513832584ab0e7ab375c35f8c2dbc50781cc
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62789332"
---
# <a name="substring-function-access-custom-web-app"></a>SubString Function (Access custom web app)

Renvoie une partie d’une expression de texte.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **SubString** (*TextExpression*, *Start*, *Length*) 
  
La **fonction SubString** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Expression de texte. |
| *Start*  <br/> |Expression de nombres integer qui spécifie l’endroit où commencent les caractères renvoyés. Si le début est inférieur à 1, l’expression renvoyée commence au premier caractère spécifié dans l’expression. Dans ce cas, le nombre de caractères renvoyés est la plus grande valeur de la somme de début + longueur - 1 ou 0. Si le début est supérieur au nombre de caractères dans l’expression de valeur, une expression de longueur nulle est renvoyée. |
| *Length*  <br/> |Expression d’un nombre nombre positif qui spécifie le nombre de caractères de l’expression qui seront renvoyés. Si la longueur est négative, une erreur est générée et l’instruction est terminée. Si la somme du début et de la longueur est supérieure au nombre de caractères dans l’expression, l’expression de valeur entière commençant au début est renvoyée. |
   

