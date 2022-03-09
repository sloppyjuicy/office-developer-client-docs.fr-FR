---
title: HASCATEGORY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Renvoie TRUE si la chaîne spécifiée est trouvée dans la liste des catégories de la forme.
ms.openlocfilehash: 212bc818f697440810a5c09c130df5a733c4e567
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63405566"
---
# <a name="hascategory-function"></a>Fonction HASCATEGORY

Renvoie TRUE si la chaîne spécifiée est trouvée dans la liste des catégories de la forme.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010

  
## <a name="syntax"></a>Syntaxe

HASCATEGORY(***category*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *category* <br/> |Requis  <br/> |**String** <br/> |Catégorie à rechercher. |

### <a name="return-value"></a>Valeur renvoyée

 **Boolean**
  
## <a name="remarks"></a>Remarques

 *Les catégories*  sont des chaînes définies par l’utilisateur que vous pouvez utiliser pour classer les formes. Vous pouvez définir les catégories dans la cellule User.msvShapeCategories dans la feuille ShapeSheet d’une forme. Vous pouvez définir plusieurs catégories pour une forme en les séparant par des points-virgules.
  