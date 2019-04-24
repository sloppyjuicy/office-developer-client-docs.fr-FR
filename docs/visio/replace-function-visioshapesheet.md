---
title: REPLACE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320159"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE Function (VisioShapeSheet)

Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
  
## <a name="syntax"></a>Syntaxe

RePLACE (* * *ancien_texte* * *, * * *no_départ* * *, * * *no_car* * *, * * *nouveau_texte* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _ancien_texte_ <br/> |Obligatoire  <br/> |**String** <br/> |Texte dans lequel vous souhaitez remplacer certains caractères.  <br/> |
| _no_départ_ <br/> |Obligatoire  <br/> |**Number** <br/> |Position du caractère d' _ancien_texte_ à remplacer par _nouveau_texte_. Le premier caractère de la chaîne est à la position 1.  <br/> |
| _no_car_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre de caractères d' _ancien_texte_ à remplacer  <br/> |
| _nouveau_texte_ <br/> |Obligatoire  <br/> |**String** <br/> |Texte qui remplace les caractères d' _ancien_texte_.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Utilisez la fonction REPLACE lorsque vous souhaitez remplacer du texte qui apparaît à un endroit spécifique dans une chaîne de texte. Pour remplacer un texte spécifique dans une chaîne de texte, utilisez la fonction SUBSTITUTE.
  
## <a name="example"></a>Exemple

REPLACE ("01/03/2002",9,2,"03") 
  
Renvoie le 01.03.03. 
  

