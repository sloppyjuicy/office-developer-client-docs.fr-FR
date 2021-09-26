---
title: FORMAT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
ms.localizationpriority: medium
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Renvoie le résultat de l’expression sous la forme d’une chaîne mise en forme selon la mise en forme.
ms.openlocfilehash: bc5af650fdb4f5012963206f24a56d4bdd1c2592
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618944"
---
# <a name="format-function"></a>Fonction FORMAT

Renvoie le résultat de  _l’expression_ sous la forme d’une chaîne mise en forme en fonction  _de formatpicture_.
  
## <a name="syntax"></a>Syntaxe

FORMAT(** *expression* **, » ** *formatpicture* ** « ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**String** <br/> |Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.  <br/> |
| _formatpicture_ <br/> |Obligatoire  <br/> |**String** <br/> |Modèle de format utilisé pour la mise en forme de la chaîne.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Le type de l’expression et celui indiqué dans le modèle de format régissent le comportement de la chaîne renvoyée. La  _mise en forme doit_ être appropriée pour le type d’expression. Pour plus d’informations sur la spécification d’images de format, voir [à propos des images de format.](about-format-pictures.md)
  
Renvoie une erreur si le résultat de  _l’expression_ et le type attendu dans  _formatpicture_ sont d’un type différent ou s’il existe des erreurs de syntaxe dans  _formatpicture_.
  
## <a name="example-1"></a>Exemple 1

FORMAT(1cm/4, "0,000 u")
  
Renvoie « 0,250 cm ».
  
## <a name="example-2"></a>Exemple 2

FORMAT(1cm/4, "0,00 U")
  
Renvoie « 0,25 CM ».
  
## <a name="example-3"></a>Exemple 3

FORMAT(1cm/4, "0,0 u")
  
Renvoie « 0,3 cm ».
  

