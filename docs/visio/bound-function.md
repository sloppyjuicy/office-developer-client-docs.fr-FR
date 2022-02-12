---
title: BOUND, fonction
manager: lindalu
ms.date: 02/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
ms.localizationpriority: medium
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Limite la valeur d’une cellule à une plage ou à un ensemble de plages.
ms.openlocfilehash: ce1fbfedf7e1f7875c6808b7b110a1ca25dc3f73
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781043"
---
# <a name="bound-function"></a>Fonction BOUND

Limite la valeur d’une cellule à une plage ou à un ensemble de plages.
  
## <a name="syntax"></a>Syntaxe

BOUND (***value**_, _*_type_*_, _*_ignore_*_, _*_value1_*_, _*_value2_*_ _*_[,ignore(n), value1(n), value2(n),...]_ ** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _value_ |Requis |**Numérique** |Valeur actuelle limitée. |
| _type_ |Obligatoire |**Numérique** |Indique si la contrainte est inclusive (0), exclusive (1) ou désactivée (2). |
| _ignore_ |Obligatoire |**Booléen** | TRUE pour ignorer la plage ; FALSE pour limiter la valeur de la cellule à la plage. |
| _value1_ |Requis |**Numérique** |Première valeur d’une plage. |
| _value2_ |Requis |**Numérique** |Deuxième valeur d’une plage. |

## <a name="remarks"></a>Remarques

Utilisez la fonction BOUND pour restreindre la valeur d’une cellule à une limite supérieure et inférieure, par exemple, pour contrôler des objets qui ne devraient pas être étirés au delà ou en deçà d’une hauteur minimale ou maximale. La contrainte peut être inclusive ou exclusive par rapport aux plages. Si la valeur actuelle ne doit pas être limitée, définissez le paramètre *type* sur 2 (désactivé).
  
Vous pouvez définir plusieurs plages en fournissant plusieurs occurrences des paramètres *ignore*, *value1* et *value2*. Utilisez le  *paramètre Ignore* pour désactiver les contraintes d’une plage particulière.
  
La formule contenant la fonction BOUND n’est pas écrasée lorsque sa valeur change ; la formule est au contraire préservée et la nouvelle valeur est placée dans le paramètre *value*.
  
## <a name="example-1"></a>Exemple1

Cet exemple utilise la fonction BOUND pour obliger une poignée de contrôle à rester à l’intérieur du rectangle de délimitation d’une forme.
  
Controls.X1 = BOUND(Width0.5\*, 0, FALSE, Width0\*, Width1\*)
  
Controls.Y1 = BOUND(Height0.5\*, 0, FALSE, Height0\*, Height1\*)
  
## <a name="example-2"></a>Exemple2

Cet exemple utilise la fonction BOUND pour limiter la largeur d’une forme à 2 pouces, 4 pouces ou 6 pouces.
  
Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)
