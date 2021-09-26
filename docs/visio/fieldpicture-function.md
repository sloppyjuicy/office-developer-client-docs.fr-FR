---
title: FIELDPICTURE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
ms.localizationpriority: medium
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Renvoie une chaîne d’image de format qui correspond au code de format Visio de champ de texte interne Microsoft.
ms.openlocfilehash: 1240386f38945dd7ede35f083ed4be87f75f5d81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619014"
---
# <a name="fieldpicture-function"></a>Fonction FIELDPICTURE

Renvoie une chaîne d’image de format qui correspond au code de format Visio de champ de texte interne Microsoft.
  
## <a name="syntax"></a>Syntaxe

FIELDPICTURE(** *code* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Obligatoire  <br/> |**Number** <br/> | Code de format de champ de texte.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Les chaînes de modèle de format sont utilisées par la fonction FORMAT pour définir le développement des valeurs en dates, heures, nombres et intitulés d’unité.
  
## <a name="example"></a>Exemple

FIELDPICTURE(0) 
  
Renvoie la chaîne de modèle de format « esc(0) », qui permet de représenter un nombre à une décimale dont l’unité est en minuscule lorsque la fonction FORMAT est utilisée. 
  

