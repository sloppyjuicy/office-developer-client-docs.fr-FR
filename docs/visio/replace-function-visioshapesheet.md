---
title: REPLACE Function (VisioShapeSheet)
manager: lindalu
ms.date: 03/09/2022
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
ms.localizationpriority: medium
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
ms.openlocfilehash: 4a11b356a9263fbc7a93520c5615cc991913d627
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404151"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE Function (VisioShapeSheet)

Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
  
## <a name="syntax"></a>Syntaxe

REPLACE (***old_text** _, _*_start_num_*_, _*_num_chars_*_, _ *_new_text_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *old_text* <br/> |Requis  <br/> |**String** <br/> |Texte dans lequel vous souhaitez remplacer certains caractères. |
| *start_num* <br/> |Requis  <br/> |**Number** <br/> |Position du caractère dans *old_text* à remplacer par *new_text*. Le premier caractère de la chaîne est à la position 1. |
| *num_chars* <br/> |Requis  <br/> |**Number** <br/> |Nombre de caractères dans *old_text* à remplacer.  <br/> |
| *new_text* <br/> |Requis  <br/> |**String** <br/> |Texte qui remplace des caractères dans *old_text*. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Utilisez la fonction REPLACE lorsque vous souhaitez remplacer du texte qui apparaît à un endroit spécifique dans une chaîne de texte. Pour remplacer un texte spécifique dans une chaîne de texte, utilisez la fonction SUBSTITUTE.
  
## <a name="example"></a>Exemple

REPLACE ("01/03/2002",9,2,"03")
  
Renvoie le 01.03.03.
  