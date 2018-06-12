---
title: FIELDPICTURE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Renvoie une chaîne de format de l’image qui établit une correspondance avec le code de format de champ de texte interne Microsoft Visio.
ms.openlocfilehash: 1528cefd65ed0c7c1dde02fa390babf26442b4d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788597"
---
# <a name="fieldpicture-function"></a>FIELDPICTURE, fonction

Renvoie une chaîne de format de l’image qui établit une correspondance avec le code de format de champ de texte interne Microsoft Visio.
  
## <a name="syntax"></a>Syntaxe

FIELDPICTURE (** *code* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Obligatoire  <br/> |**Number** <br/> | Code de format de champ de texte.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Chaîne
  
## <a name="remarks"></a>Remarques

Les chaînes de modèle de format sont utilisées par la fonction FORMAT pour définir le développement des valeurs en dates, heures, nombres et intitulés d’unité.
  
## <a name="example"></a>Exemple

FIELDPICTURE(0) 
  
Renvoie la chaîne de modèle de format « esc(0) », qui permet de représenter un nombre à une décimale dont l’unité est en minuscule lorsque la fonction FORMAT est utilisée. 
  

