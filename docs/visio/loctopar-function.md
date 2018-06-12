---
title: LOCTOPAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: Renvoie un point transformé en coordonnées parent dans le système de coordonnées de destination.
ms.openlocfilehash: 7d882ec34de93db2828fc751f99d87fc3e961d64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789059"
---
# <a name="loctopar-function"></a>LOCTOPAR, fonction

Renvoie un point transformé en coordonnées parent dans le système de coordonnées de destination.
  
## <a name="syntax"></a>Syntaxe

LOCTOPAR (** *pointSrc* **, ** *srcRef* **, ** *dstRef* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _pointSrc_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Point en coordonnées locales du système de coordonnées source  <br/> |
| _srcRef_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Référence à une cellule de l’objet source  <br/> |
| _dstRef_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Référence à une cellule de l’objet cible  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

La fonction LOCTOPAR convertit un point des coordonnées locales dans une forme source en coordonnées parent de la forme de destination. Vous pouvez utiliser la fonction LOCTOPAR pour définir des coordonnées parent dans les cellules d’une forme, comme PinX, PinY, BeginX et BeginY, en utilisant un point d’un autre système de coordonnées. 
  
Cette fonction peut être utilisée même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement lors de la transformation intermédiaire. 
  
Les coordonnées source et cible doivent se trouver sur la même page. 
  
Si la destination est une page qui n’a pas de parent, le résultat est exprimé dans les coordonnées locales de la page. 
  
## <a name="example"></a>Exemple

LOCTOPAR(PNT(LocPinX, LocPinY), Width; Feuille.4!Width) 
  
Convertit les coordonnées de l’axe local de la forme associée à la formule en coordonnées parent de Feuille.4. 
  

