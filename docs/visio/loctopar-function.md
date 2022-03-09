---
title: LOCTOPAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
ms.localizationpriority: medium
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Renvoie un point transformé dans les coordonnées parent dans le système de coordonnées de destination.
ms.openlocfilehash: 23e13609065865abdb8b120d5a67276204e61875
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404417"
---
# <a name="loctopar-function"></a>Fonction LOCTOPAR

Renvoie un point transformé dans les coordonnées parent dans le système de coordonnées de destination.
  
## <a name="syntax"></a>Syntaxe

LOCTOPAR(**_srcPoint_**, **_srcRef_**, **_dstRef_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _srcPoint_ <br/> |Requis  <br/> |**String** <br/> | Point en coordonnées locales du système de coordonnées source |
| _srcRef_ <br/> |Requis  <br/> |**String** <br/> | Référence à une cellule de l’objet source |
| _dstRef_ <br/> |Requis  <br/> |**String** <br/> | Référence à une cellule de l’objet cible |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction LOCTOPAR convertit un point des coordonnées locales dans une forme source en coordonnées parent de la forme de destination. Vous pouvez utiliser la fonction LOCTOPAR pour définir des coordonnées parent dans les cellules d’une forme, comme PinX, PinY, BeginX et BeginY, en utilisant un point d’un autre système de coordonnées.
  
Cette fonction peut être utilisée même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement dans la transformation intermédiaire.
  
Les coordonnées source et cible doivent se trouver sur la même page.
  
Si la destination est une page qui n’a pas de parent, le résultat est exprimé dans les coordonnées locales de la page.
  
## <a name="example"></a>Exemple

LOCTOPAR(PNT(LocPinX, LocPinY), Width; Feuille.4!Width)
  
Convertit les coordonnées de l’axe local de la forme associée à la formule en coordonnées parent de Feuille.4.
  