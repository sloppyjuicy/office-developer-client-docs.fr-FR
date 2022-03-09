---
title: TINT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifie la couleur en augmentant sa luminosité par la quantité (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: 82e6b047d2376028ce6e29cda3efd0e5feedecba
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404791"
---
# <a name="tint-function"></a>Fonction TINT

Modifie la couleur en augmentant sa luminosité par la quantité (positive ou négative) spécifiée dans le _paramètre int_ .
  
## <a name="syntax"></a>Syntaxe

TINT(***color** _, _ *_int_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Index de couleurs Microsoft Visio ou valeur RVB de la couleur. |
| _int_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Valeur d’augmentation de la luminosité de la couleur. Elle peut être positive ou négative. |

### <a name="return-value"></a>Valeur renvoyée

 **RGB**
  
## <a name="remarks"></a>Remarques

Les limites basse et haute de luminosité sont respectivement 0 et 240. Il n’existe pas de limite pour la taille de l’entier que vous pouvez envoyer au paramètre _int_, cependant la luminosité ne dépasse jamais ces limites.
  