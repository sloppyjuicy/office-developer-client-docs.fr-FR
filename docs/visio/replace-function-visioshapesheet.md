---
title: REPLACE, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
ms.openlocfilehash: 4112339d772248ac033674808d97c3f9c55b6f0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789438"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE, fonction (VisioShapeSheet)

Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
  
## <a name="syntax"></a>Syntaxe

Remplacer (** *old_text* **, ** *start_num* **, ** *nb_cars* **, ** *new_text* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _old_text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Texte dans lequel vous souhaitez remplacer certains caractères.  <br/> |
| _Start_num_ <br/> |Obligatoire  <br/> |**Number** <br/> |Position du caractère dans _old_text_ que vous souhaitez remplacer par _new_text_. Le premier caractère de la chaîne est la position 1.  <br/> |
| _nb_cars_ <br/> |Obligatoire  <br/> |**Number** <br/> |Le nombre de caractères dans _old_text_ que vous souhaitez remplacer  <br/> |
| _new_text_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Le texte qui remplace des caractères dans _old_text_.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

Utilisez la fonction REPLACE lorsque vous souhaitez remplacer du texte qui apparaît à un endroit spécifique dans une chaîne de texte. Pour remplacer un texte spécifique dans une chaîne de texte, utilisez la fonction SUBSTITUTE.
  
## <a name="example"></a>Exemple

REPLACE ("01/03/2002",9,2,"03") 
  
Renvoie le 01.03.03. 
  

