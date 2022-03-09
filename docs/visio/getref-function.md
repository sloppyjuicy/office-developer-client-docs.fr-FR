---
title: GETREF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
ms.localizationpriority: medium
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencé change.
ms.openlocfilehash: 4c943c9c91e38c9aac1da7950e987a8a99c3e304
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404375"
---
# <a name="getref-function"></a>Fonction GETREF

Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencé change.
  
## <a name="syntax"></a>Syntaxe

GETREF(***cellname*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *cellname* <br/> |Requis  <br/> |**String** <br/> |Nom de la cellule à qui obtenir une référence. |

## <a name="example"></a>Exemple

SETF(GETREF(PinX),5.1)
  
Donne à la formule de la cellule PinX la valeur 5,1.
  