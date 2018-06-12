---
title: HASCATEGORY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Renvoie TRUE si la chaîne spécifiée est trouvée dans la liste des catégories de la forme.
ms.openlocfilehash: 2445b4c3af63b331b303897997ce38b0747f17fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788765"
---
# <a name="hascategory-function"></a>HASCATEGORY, fonction

Renvoie TRUE si la chaîne spécifiée est trouvée dans la liste des catégories de la forme.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010 
  
## <a name="syntax"></a>Syntaxe

HASCATEGORY (** *catégorie* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _category_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Catégorie à rechercher.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

 **Booléen**
  
## <a name="remarks"></a>Notes

 *Les catégories* sont des chaînes définies par l’utilisateur que vous pouvez utiliser pour classer les formes. Vous pouvez définir des catégories dans la cellule User.msvShapeCategories dans la feuille ShapeSheet d’une forme. Vous pouvez définir plusieurs catégories d’une forme en séparant les catégories par des points-virgules. 
  

