---
title: CONTAINERSHEETREF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Renvoie une référence de feuille au conteneur spécifié contenant la forme.
ms.openlocfilehash: 6392b4c1a2652f1a831dc585c0be0f430a5ffe0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788357"
---
# <a name="containersheetref-function"></a>CONTAINERSHEETREF, fonction

Renvoie une référence de feuille au conteneur spécifié contenant la forme.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010 
  
## <a name="syntax"></a>Syntaxe

CONTAINERSHEETREF (** *index* ** ** *[, catégorie]* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |Obligatoire  <br/> |**Integer** <br/> |Index de base 1 du conteneur. Voir la section Remarques pour plus d’informations.  <br/> |
| _category_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Catégorie du conteneur. Voir la section Remarques pour plus d’informations.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Référence ShapeSheet
  
## <a name="remarks"></a>Note

L’index d’un conteneur est calculé en fonction de l’ordre de plan des conteneurs d’avant en arrière.
  
 *Les catégories* sont des chaînes définies par l’utilisateur que vous pouvez utiliser pour classer les formes. Vous pouvez définir des catégories dans la cellule User.msvShapeCategories dans la feuille ShapeSheet d’une forme. Vous pouvez définir plusieurs catégories d’une forme en séparant les catégories par des points-virgules. 
  
Si la forme n’est pas membre d’un conteneur, ou si aucun conteneur ne correspond à l’index spécifié et à la catégorie, CONTAINERSHEETREF renvoie #REF!.
  
## <a name="example"></a>Exemple

CONTAINERSHEETREF(1)!Height 
  
Renvoie la valeur de la cellule Height du conteneur le plus en avant sur la page à laquelle appartient la forme. 
  

