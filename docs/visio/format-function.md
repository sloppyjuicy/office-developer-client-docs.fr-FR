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
description: Renvoie le résultat de l’expression sous la forme d’une chaîne mise en forme en fonction de formatpicture.
ms.openlocfilehash: 6704e80bbbff91114f66aa671745de8ff66df3a4
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771544"
---
# <a name="format-function"></a>Fonction FORMAT

Renvoie le résultat de  _l’expression_ sous la forme d’une chaîne mise en forme en fonction de  _formatpicture_.
  
## <a name="syntax"></a>Syntaxe

FORMAT(** *expression* **, » ** *formatpicture* ** « ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Requis  <br/> |**String** <br/> |Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur. |
| _formatpicture_ <br/> |Requis  <br/> |**String** <br/> |Modèle de format utilisé pour la mise en forme de la chaîne. |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Le type de l’expression et celui indiqué dans le modèle de format régissent le comportement de la chaîne renvoyée. La  _mise en forme doit_ être appropriée pour le type d’expression. Pour plus d’informations sur la spécification d’images de format, voir [À propos des images de format](about-format-pictures.md).
  
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
  

