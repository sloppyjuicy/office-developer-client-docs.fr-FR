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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414493"
---
# <a name="msoshade-function"></a>Fonction MSOSHADE

Modifie la couleur en diminuant sa luminosité du pourcentage spécifié.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

MS CRYPTODE(** *color* **, ** *-deltaLum* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**RVB** <br/> |Valeur de couleur RVB (rouge, vert, bleu) standard ou référence à une couleur.  <br/> |
| _-deltaLum_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Le pourcentage de changement vers le blanc (-100 %) ou noir (100 %) à partir de  _la valeur de_ couleur.  <br/> |
   
## <a name="remarks"></a>Remarques

Plus la valeur  _de couleur_ est proche du blanc ou du noir, plus la modification de l’ombre produite par une valeur  _-deltaLum_ spécifique est faible. 
  

