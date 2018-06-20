---
title: Fonction de sélections (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Insère une chaîne de texte dans une autre chaîne de texte. Elle supprime une longueur de caractères dans la première chaîne à la position de début spécifiée et insère ensuite la deuxième chaîne dans la première chaîne de la position de début.
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781986"
---
# <a name="stuff-function-access-custom-web-app"></a>Fonction de sélections (accès personnalisé web app)

Insère une chaîne de texte dans une autre chaîne de texte. Elle supprime une longueur de caractères dans la première chaîne à la position de début spécifiée et insère ensuite la deuxième chaîne dans la première chaîne de la position de début.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Sélections** (*IntoTextExpression*, *début*, *longueur*, *ThisTextExpression*) 
  
La fonction de **document** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Une expression de texte qui spécifie le texte dans lequel le texte spécifié par le *ThisTextExpression* sera inséré.  <br/> |
| *Début*  <br/> |Entier qui spécifie l’emplacement pour démarrer l’insertion et suppression. Si start ou length est négatif, une chaîne nulle est renvoyée. Si start est plus long que premier *IntoTextExpression* , une chaîne nulle est renvoyée.  <br/> |
| *Length*  <br/> |Entier qui spécifie le nombre de caractères à supprimer. Si length est plus longue que première *IntoTextExpression* , suppression s’effectue jusqu’au dernier caractère de dernière *IntoTextExpression* .  <br/> |
| *ThisTextExpression*  <br/> |Chapeau expression texte spécifie le texte à insérer dans *IntoTextExpression* . Cette expression remplacera les caractères de longueur de *IntoTextExpression* en commençant à *Démarrer* .  <br/> |
   
## <a name="remarks"></a>Remarques

Si les arguments *Start* ou *Length* sont négatifs, ou si la position de début est supérieure à la longueur de la première chaîne, une chaîne nulle est renvoyée. Si la position de début est 0, une valeur nulle est renvoyée. Si la longueur à effacer est supérieure à la première chaîne, il est supprimé au premier caractère dans la première chaîne. 
  

