---
title: FORMAT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Renvoie le résultat d'expression sous la forme d'une chaîne mise en forme conformément à formatPicture.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339892"
---
# <a name="format-function"></a>Fonction FORMAT

Renvoie le résultat d' _expression_ sous la forme d'une chaîne mise en forme conformément à _formatPicture_.
  
## <a name="syntax"></a>Syntaxe

FORMAT (* * *expression* * *, "* * *formatPicture* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**String** <br/> |Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.  <br/> |
| _formatPicture_ <br/> |Obligatoire  <br/> |**String** <br/> |Modèle de format utilisé pour la mise en forme de la chaîne.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Le type de l’expression et celui indiqué dans le modèle de format régissent le comportement de la chaîne renvoyée. Le _formatPicture_ doit être approprié pour le type d'expression. Pour plus d'informations sur la spécification des images de format, voir [à propos de la mise en forme des images](about-format-pictures.md).
  
Renvoie une erreur si le résultat d' _expression_ et le type attendu dans _formatPicture_ sont de même nature ou s'il existe des erreurs de syntaxe dans _formatPicture_.
  
## <a name="example-1"></a>Exemple 1

FORMAT(1cm/4, "0,000 u")
  
Renvoie « 0,250 cm ».
  
## <a name="example-2"></a>Exemple 2

FORMAT(1cm/4, "0,00 U")
  
Renvoie « 0,25 CM ».
  
## <a name="example-3"></a>Exemple 3

FORMAT(1cm/4, "0,0 u")
  
Renvoie « 0,3 cm ».
  

