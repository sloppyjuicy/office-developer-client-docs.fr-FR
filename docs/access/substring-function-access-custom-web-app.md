---
title: Fonction sous-chaîne (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Renvoie une partie d’une expression de texte.
ms.openlocfilehash: 49d9afefe4b25d91738e518e0ddb2b902067c038
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781998"
---
# <a name="substring-function-access-custom-web-app"></a>Fonction sous-chaîne (accès personnalisé web app)

Renvoie une partie d’une expression de texte.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Sous-chaîne** (*TextExpression*, *début*, *longueur*) 
  
La fonction de **sous-chaîne** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Une expression de texte.  <br/> |
| *Début*  <br/> |Entier qui spécifie où commencer les caractères renvoyées. Si start est inférieur à 1, l’expression renvoyée commence au premier caractère spécifié dans une expression. Dans ce cas, le nombre de caractères qui sont renvoyés est la plus grande valeur soit la somme de début + longueur-1 ou 0. Si start est supérieur au nombre de caractères dans l’expression de valeur, une expression de longueur nulle est renvoyée.  <br/> |
| *Length*  <br/> |Une expression d’entier positif qui spécifie le nombre de caractères de l’expression à retourner. Si length est négatif, une erreur est générée et l’instruction est terminée. Si la somme des start et length est supérieure au nombre de caractères dans une expression, la valeur entière expression en commençant à démarrer est renvoyée.  <br/> |
   

