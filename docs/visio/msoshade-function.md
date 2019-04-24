---
title: MSOSHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283709"
---
# <a name="msoshade-function"></a>Fonction MSOSHADE

Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

MSOSHADE (* * *couleur* * *, * * *-deltaLum* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**RVB** <br/> |Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur.  <br/> |
| _-deltaLum_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Pourcentage de changement vers blanc (-100%) ou noir (100%) de la valeur de _couleur_ .  <br/> |
   
## <a name="remarks"></a>Remarques

Plus la valeur de _couleur_ est proche de blanc ou noir, plus le changement de dégradé généré par une valeur _-deltaLum_ spécifique est faible. 
  

