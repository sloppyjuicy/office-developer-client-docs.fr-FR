---
title: BOUND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Limite la valeur d’une cellule à une plage ou à un ensemble de plages.
ms.openlocfilehash: 2f6228828fee8fa1831bb0d3a714fca068808652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788195"
---
# <a name="bound-function"></a>BOUND, fonction

Limite la valeur d’une cellule à une plage ou à un ensemble de plages.
  
## <a name="syntax"></a>Syntaxe

LIÉ (** *valeur* **, ** *type* **, ** *Ignorer* **, ** *valeur1* **, ** *valeur2* ** ** * [, ignore(n), value1(n), value2(n),...] * **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _valeur_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Valeur actuelle limitée.  <br/> |
| _type_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Si la contrainte est inclusive (0), exclusive (1) ou désactivée (2).  <br/> |
| _Ignorer_ <br/> |Obligatoire  <br/> |**Boolean** <br/> | TRUE pour ignorer la plage ; Valeur FALSE pour limiter la valeur de la cellule à la plage.  <br/> |
| _valeur1_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Première valeur dans une plage.  <br/> |
| _valeur2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Deuxième valeur d’une plage.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez la fonction BOUND pour restreindre la valeur à une limite supérieure d’une cellule et limite inférieure, par exemple, pour contrôler des objets qui ne doivent pas être étirés au-dessus ou au-dessous d’une hauteur minimale ou maximale. La contrainte peut être inclus ou exclus en ce qui concerne l’ou les plages. Si la valeur actuelle ne doit pas être limitée, définissez le paramètre _type_ sur 2 (désactivé). 
  
Vous pouvez définir plusieurs plages en fournissant plusieurs occurrences des paramètres _ignore_, _value1_et _value2_ . Pour désactiver des contraintes à une plage donnée, utilisez le paramètre _Ignorer_ . 
  
La formule contenant la fonction BOUND n’est pas écrasée lorsque sa valeur change ; au lieu de cela, la formule est préservée et la nouvelle valeur est placée dans le paramètre _value_ . 
  
## <a name="example-1"></a>Exemple1

Cet exemple utilise la fonction BOUND pour obliger une poignée de contrôle à rester à l’intérieur du rectangle de délimitation d’une forme. 
  
Controls.X1 = liés aux (largeur\*0,5, 0, la valeur FALSE, la largeur\*largeur 0,\*1)
  
Controls.Y1 = liés aux (hauteur\*0,5, 0, la valeur FALSE, la hauteur\*hauteur 0,\*1)
  
## <a name="example-2"></a>Exemple2

Cet exemple utilise la fonction BOUND pour limiter la largeur d’une forme à 2 pouces, 4 pouces ou 6 pouces. 
  
Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)
  

