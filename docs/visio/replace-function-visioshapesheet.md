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
ms.openlocfilehash: 64dcd886ce9c357d0f9bd7aa735231ceba3f76ca
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62772703"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE Function (VisioShapeSheet)

Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
  
## <a name="syntax"></a>Syntaxe

REPLACE (** *old_text* **, ** *start_num* **, ** *num_chars* **, ** *new_text* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _old_text_ <br/> |Requis  <br/> |**String** <br/> |Texte dans lequel vous souhaitez remplacer certains caractères. |
| _start_num_ <br/> |Requis  <br/> |**Number** <br/> |Position du caractère dans le  _old_text_ que vous souhaitez remplacer par  _new_text_. Le premier caractère de la chaîne est à la position 1. |
| _num_chars_ <br/> |Requis  <br/> |**Number** <br/> |Nombre de caractères  _dans old_text_ que vous souhaitez remplacer  <br/> |
| _new_text_ <br/> |Requis  <br/> |**String** <br/> |Texte qui remplace les caractères dans  _old_text_. |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Utilisez la fonction REPLACE lorsque vous souhaitez remplacer du texte qui apparaît à un endroit spécifique dans une chaîne de texte. Pour remplacer un texte spécifique dans une chaîne de texte, utilisez la fonction SUBSTITUTE.
  
## <a name="example"></a>Exemple

REPLACE ("01/03/2002",9,2,"03") 
  
Renvoie le 01.03.03. 
  

