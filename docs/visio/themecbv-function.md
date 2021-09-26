---
title: Fonction THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Renvoie une valeur RVB ou un nombre qui représente un index dans la palette de couleurs du document, où la couleur (nombre) passée en tant qu’argument a été modifiée par la teinte ou la valeur de nuance spécifiée stockée dans les paramètres de dégradé du thème actif.
ms.openlocfilehash: 1d9a95aedee2f04e72bd4868ddfaec149c872b62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603327"
---
# <a name="themecbv-function"></a>Fonction THEMECBV

Renvoie une valeur RVB ou un nombre qui représente un index dans la palette de couleurs du document, où la couleur (nombre) passée en tant qu’argument a été modifiée par la teinte ou la valeur de nuance spécifiée stockée dans les paramètres de dégradé du thème actif. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013
 
  
## <a name="syntax"></a>Syntaxe

 **THEMECBV**( _couleur_,  _gradient_stop_number_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre représentant un index dans la palette de couleurs du document.  <br/> |
| _gradient_stop_number_ <br/> |Obligatoire  <br/> |**Number** <br/> |L’arrêt de dégradé (teinte ou ombre) stocké dans les paramètres de dégradé du thème actif à appliquer à la couleur.  <br/> |
   
## <a name="return-value"></a>Valeur renvoyée

 **Number**
  
## <a name="remarks"></a>Remarques

> [!NOTE]
> La fonction THEMECBV ne fait rien à la couleur transmise en tant qu’argument si le QuickStyle qui est affecté à la forme n’a pas de dégradé. 
  
Les paramètres de dégradé d’un thème sont une série d’arrêts de dégradé numérotés qui correspondent à un « éclaircissement » (teinte) ou à un assombrissement (ombre). Ces nuances et teintes sont appliquées à une couleur de base pour créer un effet de dégradé de couleur.
  
La **fonction THEMECBV** prend une entrée de couleur et produit la couleur après avoir été modifiée par la teinte ou l’ombre de l’arrêt de dégradé spécifié. Les teintes et nuances proviennent de la définition du thème, si le style rapide actuel contient un remplissage en dégradé. Si le style rapide actif ne spécifie pas de remplissage dégradé ou si la forme est définie sur Aucun thème, cette formule renvoie simplement la couleur qui a été passée pour le premier argument. 
  
## <a name="example"></a>Exemple

 `THEMECBV(FillForegnd, 5)`
  
Renvoie la couleur créée en appliquant la teinte ou l’ombre du cinquième dégradé du dégradé à la couleur spécifiée dans la **cellule FillForegnd.** 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Renvoie une nuance ou une teinte de rouge créée en appliquant le deuxième point de dégradé à une couleur de base de rouge.
  

