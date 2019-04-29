---
title: POW, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Renvoie un nombre élevé à la puissance d'un exposant.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406310"
---
# <a name="pow-function"></a>Fonction POW

Renvoie un nombre élevé à la puissance d'un exposant.
  
## <a name="syntax"></a>Syntaxe

POW (* * *nombre* * *, * * *exposant* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre à élever à la puissance d’un exposant  <br/> |
| _exposant_ <br/> |Obligatoire  <br/> |**Number** <br/> |Exposant  <br/> |
   
## <a name="remarks"></a>Remarques

Le _nombre_ et l' _exposant_ peuvent être des nombres autres que des entiers, et ils peuvent être négatifs. Si le _nombre_ n'est pas 0 et que l' _exposant_ est égal à 0, cette fonction renvoie la valeur 1. Si _nombre_ est égal à 0 et _exposant_ est négatif, cette fonction renvoie 0,0. Si le _nombre_ et l' _exposant_ sont 0, ou si le _nombre_ est négatif et l' _exposant_ n'est pas un entier, cette fonction renvoie 0,0. Si le _nombre_ et l' _exposant_ sont négatifs, cette fonction renvoie la valeur-1. #IND. 
  
## <a name="example"></a>Exemple

POW (5, 2) 
  
Renvoie 25. 
  

