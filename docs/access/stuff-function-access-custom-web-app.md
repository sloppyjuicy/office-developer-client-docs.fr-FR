---
title: Fonction Stuff (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Insère une chaîne de texte dans une autre chaîne de texte. Il supprime une longueur spécifiée de caractères dans la première chaîne à la position de début, puis insère la deuxième chaîne dans la première chaîne à la position de début.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427674"
---
# <a name="stuff-function-access-custom-web-app"></a>Fonction Stuff (application Web personnalisée Access)

Insère une chaîne de texte dans une autre chaîne de texte. Il supprime une longueur spécifiée de caractères dans la première chaîne à la position de début, puis insère la deuxième chaîne dans la première chaîne à la position de début.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **** Éléments (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*) 
  
La fonction **Stuff** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Expression de texte qui spécifie le texte dans lequel le texte spécifié par l' *ThisTextExpression* sera inséré.  <br/> |
| *Start*  <br/> |Valeur entière qui spécifie l'emplacement de début de la suppression et de l'insertion. Si start ou length est négatif, une chaîne nulle est renvoyée. Si Start est plus long que le premier *IntoTextExpression* , une chaîne nulle est renvoyée.  <br/> |
| *Length*  <br/> |Entier qui spécifie le nombre de caractères à supprimer. Si length est plus long que le premier *IntoTextExpression* , la suppression se produit jusqu'au dernier caractère du dernier *IntoTextExpression* .  <br/> |
| *ThisTextExpression*  <br/> |Un chapeau d'expression de texte spécifie le texte à insérer dans *IntoTextExpression* . Cette expression remplace les caractères de longueur de *IntoTextExpression* en commençant au *début* .  <br/> |
   
## <a name="remarks"></a>Remarques

Si les arguments *Start* ou *Length* sont négatifs, ou si la position de départ est supérieure à la longueur de la première chaîne, une chaîne NULL est renvoyée. Si la position de début est 0, une valeur null est renvoyée. Si la longueur à supprimer est supérieure à la première chaîne, elle est supprimée jusqu'au premier caractère de la première chaîne. 
  

