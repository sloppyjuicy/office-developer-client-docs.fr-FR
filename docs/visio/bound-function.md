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
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425959"
---
# <a name="bound-function"></a>Fonction BOUND

Limite la valeur d’une cellule à une plage ou à un ensemble de plages.
  
## <a name="syntax"></a>Syntaxe

BOUND (* * *value* * *, * * *type* * *, * * *ignore* * *, * * *value1* * *, * * *value2* * * * * * [, ignore (n), value1 (n), valeur2 (n),...] * * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Valeur actuelle limitée.  <br/> |
| _type_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Indique si la contrainte est inclusive (0), exclusive (1) ou désactivée (2).  <br/> |
| _Passez_ <br/> |Obligatoire  <br/> |**Booléen** <br/> | TRUE pour ignorer la plage; FALSe pour limiter la valeur de la cellule à la plage.  <br/> |
| _valeur1,valeur2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Première valeur d’une plage.  <br/> |
| _valeur2_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Deuxième valeur d’une plage.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez la fonction BOUND pour restreindre la valeur d’une cellule à une limite supérieure et inférieure, par exemple, pour contrôler des objets qui ne devraient pas être étirés au delà ou en deçà d’une hauteur minimale ou maximale. La contrainte peut être inclusive ou exclusive par rapport aux plages. Si la valeur actuelle ne doit pas être restreinte, définissez le paramètre _type_ sur 2 (Disabled). 
  
Vous pouvez définir plusieurs plages en fournissant plusieurs occurrences des paramètres _ignore_, _value1_et _value2_ . Utilisez le __ paramètre ignore pour désactiver les contraintes d'une plage particulière. 
  
La formule contenant la fonction BOUND n'est pas remplacée lorsque sa valeur change; au lieu de cela, la formule est conservée et la nouvelle valeur est placée dans le paramètre _value_ . 
  
## <a name="example-1"></a>Exemple1

Cet exemple utilise la fonction BOUND pour obliger une poignée de contrôle à rester à l’intérieur du rectangle de délimitation d’une forme. 
  
Controls. X1 = BOUND (\*largeur 0,5, 0, faux,\*largeur 0,\*largeur 1)
  
Controls. Y1 = BOUND (\*hauteur 0,5, 0, false\*, hauteur 0\*, hauteur 1)
  
## <a name="example-2"></a>Exemple2

Cet exemple utilise la fonction BOUND pour limiter la largeur d’une forme à 2 pouces, 4 pouces ou 6 pouces. 
  
Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)
  

