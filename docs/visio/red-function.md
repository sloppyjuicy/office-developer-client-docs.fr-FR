---
title: RED, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Renvoie la composante rouge d’une couleur.
ms.openlocfilehash: 801ebb64564df81f72c41cb720fe53f0f1b4c10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19789392"
---
# <a name="red-function"></a>RED, fonction

Renvoie la composante rouge d’une couleur. 
  
## <a name="syntax"></a>Syntaxe

ROUGE (** *expression* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**Varie** <br/> |Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Nombre
  
## <a name="remarks"></a>Note

La valeur de retour est un nombre compris entre 0 et 255, inclus, ou une référence de cellule qui correspond à un index. Si _expression_ n’est pas valide, cette fonction renvoie 0 (noir). 
  
## <a name="example-1"></a>Exemple 1

RED(22)
  
Renvoie 51 si le document utilise la palette de couleurs par défaut de Microsoft Office Visio, où le gris foncé a l’index de couleur 22.
  
## <a name="example-2"></a>Exemple 2

Red(char.Color)
  
Renvoie la valeur de la composante rouge de la couleur de police actuelle.
  
## <a name="example-3"></a>Exemple 3

RED(RVB(10, 20, 30))
  
Renvoie 10.
  

