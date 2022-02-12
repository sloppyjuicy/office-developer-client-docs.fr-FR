---
title: CONTAINERSHEETREF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Renvoie une référence de feuille au conteneur spécifié contenant la forme.
ms.openlocfilehash: 99793b7fc24de0dd682e34d3073b0ccd9a53fcfa
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782331"
---
# <a name="containersheetref-function"></a>Fonction CONTAINERSHEETREF

Renvoie une référence de feuille au conteneur spécifié contenant la forme.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

CONTAINERSHEETREF(** *index* ** ** *[, category]* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Index de base 1 du conteneur. Voir la section Remarques pour plus d’informations. |
| _category_ <br/> |Facultatif  <br/> |**Chaîne** <br/> |Catégorie du conteneur. Voir la section Remarques pour plus d’informations. |
   
### <a name="return-value"></a>Valeur renvoyée

Référence ShapeSheet
  
## <a name="remarks"></a>Remarques

L’index d’un conteneur est calculé en fonction de l’ordre de plan des conteneurs d’avant en arrière.
  
 *Les catégories*  sont des chaînes définies par l’utilisateur que vous pouvez utiliser pour classer les formes. Vous pouvez définir les catégories dans la cellule User.msvShapeCategories dans la feuille ShapeSheet d’une forme. Vous pouvez définir plusieurs catégories pour une forme en les séparant par des points-virgules. 
  
Si la forme n’est pas membre d’un conteneur, ou si aucun conteneur ne correspond à l’index spécifié et à la catégorie, CONTAINERSHEETREF renvoie #REF!.
  
## <a name="example"></a>Exemple

CONTAINERSHEETREF(1)! Height 
  
Renvoie la valeur de la cellule Height du conteneur le plus en avant sur la page à laquelle appartient la forme. 
  

