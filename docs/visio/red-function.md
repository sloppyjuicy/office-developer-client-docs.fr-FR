---
title: RED, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
ms.localizationpriority: medium
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Renvoie le composant rouge d’une couleur.
ms.openlocfilehash: 37d54cb5cb35bb285b92ab31eea8482709410911
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623137"
---
# <a name="red-function"></a>Fonction RED

Renvoie le composant rouge d’une couleur. 
  
## <a name="syntax"></a>Syntaxe

RED(** *expression* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> |Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Nombre
  
## <a name="remarks"></a>Remarques

La valeur renvoyée est un nombre compris entre 0 et 255 inclus ou une référence de cellule correspondant à un index. Si  _l’expression_ n’est pas valide, cette fonction renvoie 0 (noir). 
  
## <a name="example-1"></a>Exemple 1

RED(22)
  
Renvoie 51 si le document utilise la palette de couleurs par défaut de Microsoft Office Visio, où le gris foncé a l’index de couleur 22.
  
## <a name="example-2"></a>Exemple 2

RED(Char.Color)
  
Renvoie la valeur de la composante rouge de la couleur de police actuelle.
  
## <a name="example-3"></a>Exemple 3

RED(RVB(10, 20, 30))
  
Renvoie 10.
  

