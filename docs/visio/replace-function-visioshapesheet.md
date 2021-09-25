---
title: REPLACE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
ms.localizationpriority: medium
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
ms.openlocfilehash: 1288d18d148abc0e5bafe7fe855d140cc4e62d91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554102"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE Function (VisioShapeSheet)

Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
  
## <a name="syntax"></a>Syntaxe

REPLACE (** *old_text* **, ** *start_num* **, ** *num_chars* **, ** *new_text* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _old_text_ <br/> |Obligatoire  <br/> |**String** <br/> |Texte dans lequel vous souhaitez remplacer certains caractères.  <br/> |
| _start_num_ <br/> |Obligatoire  <br/> |**Number** <br/> |Position du caractère dans la  _old_text_ que vous souhaitez remplacer par  _new_text_. Le premier caractère de la chaîne est à la position 1.  <br/> |
| _num_chars_ <br/> |Obligatoire  <br/> |**Number** <br/> |Nombre de caractères  _dans old_text_ que vous souhaitez remplacer  <br/> |
| _new_text_ <br/> |Obligatoire  <br/> |**String** <br/> |Texte qui remplace les caractères dans  _old_text_.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Utilisez la fonction REPLACE lorsque vous souhaitez remplacer du texte qui apparaît à un endroit spécifique dans une chaîne de texte. Pour remplacer un texte spécifique dans une chaîne de texte, utilisez la fonction SUBSTITUTE.
  
## <a name="example"></a>Exemple

REPLACE ("01/03/2002",9,2,"03") 
  
Renvoie le 01.03.03. 
  

