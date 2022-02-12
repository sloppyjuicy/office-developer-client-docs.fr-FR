---
title: HASCATEGORY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Renvoie TRUE si la chaîne spécifiée est trouvée dans la liste des catégories de la forme.
ms.openlocfilehash: 65786db68e5be4ec6b83ce17963cc79332ff7772
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771382"
---
# <a name="hascategory-function"></a>Fonction HASCATEGORY

Renvoie TRUE si la chaîne spécifiée est trouvée dans la liste des catégories de la forme.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

HASCATEGORY(** *category* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _category_ <br/> |Requis  <br/> |**String** <br/> |Catégorie à rechercher. |
   
### <a name="return-value"></a>Valeur renvoyée

 **Boolean**
  
## <a name="remarks"></a>Remarques

 *Les catégories*  sont des chaînes définies par l’utilisateur que vous pouvez utiliser pour classer les formes. Vous pouvez définir les catégories dans la cellule User.msvShapeCategories dans la feuille ShapeSheet d’une forme. Vous pouvez définir plusieurs catégories pour une forme en les séparant par des points-virgules. 
  

