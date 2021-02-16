---
title: SubString Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Renvoie une partie d’une expression de texte.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433471"
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
| *Démarrage*  <br/> |Expression d’un nombre integer qui spécifie l’endroit où commencent les caractères renvoyés. Si le début est inférieur à 1, l’expression renvoyée commence au premier caractère spécifié dans l’expression. Dans ce cas, le nombre de caractères renvoyés est la plus grande valeur de la somme de début + longueur - 1 ou 0. Si le début est supérieur au nombre de caractères dans l’expression de valeur, une expression de longueur nulle est renvoyée.  <br/> |
| *Length*  <br/> |Expression d’un nombre integer positif qui spécifie le nombre de caractères de l’expression qui seront renvoyés. Si la longueur est négative, une erreur est générée et l’instruction est terminée. Si la somme du début et de la longueur est supérieure au nombre de caractères dans l’expression, l’expression de valeur entière commençant au début est renvoyée.  <br/> |
   

