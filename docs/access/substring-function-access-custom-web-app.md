---
title: SubString Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Renvoie une partie d’une expression de texte.
ms.openlocfilehash: 74bd29717caa32aa9a8de5376ce7fc06bef02462
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614667"
---
# <a name="substring-function-access-custom-web-app"></a>SubString Function (Access custom web app)

Renvoie une partie d’une expression de texte.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **SubString** (*TextExpression*, *Start*, *Length*) 
  
La **fonction SubString** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Expression de texte.  <br/> |
| *Start*  <br/> |Expression d’un nombre integer qui spécifie l’endroit où commencent les caractères renvoyés. Si le début est inférieur à 1, l’expression renvoyée commence au premier caractère spécifié dans l’expression. Dans ce cas, le nombre de caractères renvoyés est la plus grande valeur de la somme de début + longueur - 1 ou 0. Si le début est supérieur au nombre de caractères dans l’expression de valeur, une expression de longueur nulle est renvoyée.  <br/> |
| *Length*  <br/> |Expression d’un nombre integer positif qui spécifie le nombre de caractères de l’expression qui seront renvoyés. Si la longueur est négative, une erreur est générée et l’instruction est terminée. Si la somme du début et de la longueur est supérieure au nombre de caractères dans l’expression, l’expression de valeur entière commençant au début est renvoyée.  <br/> |
   

