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
description: Renvoie une chaîne format-image qui correspond au code de format de champ de texte interne Microsoft Visio.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431455"
---
# <a name="fieldpicture-function"></a>Fonction FIELDPICTURE

Renvoie une chaîne format-image qui correspond au code de format de champ de texte interne Microsoft Visio.
  
## <a name="syntax"></a>Syntaxe

FIELDPICTURE (* * *code* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Obligatoire  <br/> |**Number** <br/> | Code de format de champ de texte.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Les chaînes de modèle de format sont utilisées par la fonction FORMAT pour définir le développement des valeurs en dates, heures, nombres et intitulés d’unité.
  
## <a name="example"></a>Exemple

FIELDPICTURE (0) 
  
Renvoie la chaîne de modèle de format « esc(0) », qui permet de représenter un nombre à une décimale dont l’unité est en minuscule lorsque la fonction FORMAT est utilisée. 
  

