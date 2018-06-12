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
description: Renvoie le résultat d’expression sous forme de chaîne mise en forme selon formatpicture.
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788690"
---
# <a name="format-function"></a>FORMAT, fonction

Renvoie le résultat _d’expression_ sous forme de chaîne mise en forme selon _formatpicture_.
  
## <a name="syntax"></a>Syntaxe

FORMAT (** *expression* **, « ** *formatpicture* ** ») 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Combinaison de constantes, d’opérateurs, de fonctions et de références à des cellules ShapeSheet constituant une valeur.  <br/> |
| _formatPicture_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Modèle de format utilisé pour la mise en forme de la chaîne.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

Le type de l’expression et le type spécifié dans le modèle de format régissent le comportement de la chaîne retournée. Le _formatpicture_ doit être approprié pour le type d’expression. Pour plus d’informations sur la spécification des modèles de format, voir [à propos des images de format](about-format-pictures.md).
  
Renvoie une erreur si le résultat de _l’expression_ et le type attendu dans _formatpicture_ est de même nature ou s’il existe des erreurs de syntaxe dans _formatpicture_.
  
## <a name="example-1"></a>Exemple 1

FORMAT(1cm/4, "0,000 u")
  
Renvoie « 0,250 cm ».
  
## <a name="example-2"></a>Exemple 2

FORMAT(1cm/4, "0,00 U")
  
Renvoie « 0,25 CM ».
  
## <a name="example-3"></a>Exemple 3

FORMAT(1cm/4, "0,0 u")
  
Renvoie « 0,3 cm ».
  

