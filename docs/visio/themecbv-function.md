---
title: Fonction THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Renvoie une valeur RVB ou un entier qui représente un index dans la palette de couleurs, où la couleur (nombre) passée en tant qu’argument a été modifiée par la valeur spécifiée de teinte ou l’ombre stockée dans les paramètres de dégradé du thème actif.
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789895"
---
# <a name="themecbv-function"></a>Fonction THEMECBV

Renvoie une valeur RVB ou un entier qui représente un index dans la palette de couleurs, où la couleur (nombre) passée en tant qu’argument a été modifiée par la valeur spécifiée de teinte ou l’ombre stockée dans les paramètres de dégradé du thème actif. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013 
  
## <a name="syntax"></a>Syntaxe

 **THEMECBV** ( _couleur_, _gradient_stop_number_)
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre représentant un index dans la palette de couleurs.  <br/> |
| _gradient_stop_number_ <br/> |Obligatoire  <br/> |**Number** <br/> |Le point de dégradé (teinte ou l’ombre) stockée dans les paramètres de dégradé à appliquer à la couleur du thème actif.  <br/> |
   
## <a name="return-value"></a>Valeur renvoy�e

 **Number**
  
## <a name="remarks"></a>Remarques

> [!NOTE]
> La fonction THEMECBV n’a aucun effet sur la couleur passée en tant qu’argument si la propriété QuickStyle qui est affectée à la forme n’est pas un dégradé. 
  
Les paramètres de dégradé dans un thème sont une série de points de dégradé numérotée qui correspondent à un « ECLAIRCISSANT » (teinte) ou le « assombrissement » (ombre). Ces nuances et teintes sont appliqués à une couleur de base pour créer un effet de dégradé.
  
La fonction **THEMECBV** prend une entrée de couleur et renvoie la couleur une fois qu’il a été modifié par la teinte ou l’ombre du point de dégradé spécifié. Les teintes et les ombres provenant de la définition du thème, si le style rapide actuel contient un remplissage en dégradé. Si le Style rapide active ne spécifie pas un remplissage en dégradé ou la forme est définie sur aucun thème, cette formule renvoie simplement la couleur qui a été passée dans pour le premier argument. 
  
## <a name="example"></a>Exemple

 `THEMECBV(FillForegnd, 5)`
  
Renvoie la couleur créée en appliquant la teinte ou l’ombre de la cinquième de dégradé du dégradé à la couleur spécifiée dans la cellule **FillForegnd** . 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Renvoie une ombre ou teinte de rouge créé en appliquant le deuxième point de dégradé à une couleur de base de rouge.
  

