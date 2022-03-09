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
ms.openlocfilehash: 78a230653beb6eaa6d5a8376ecba6903af938b89
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404742"
---
# <a name="fieldpicture-function"></a>Fonction FIELDPICTURE

Renvoie une chaîne d’image de format qui correspond au code de format Visio de champ de texte interne Microsoft.
  
## <a name="syntax"></a>Syntaxe

FIELDPICTURE(**code*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *code* <br/> |Requis  <br/> |**Number** <br/> | Code de format de champ de texte. |

### <a name="return-value"></a>Valeur renvoyée

Chaîne
  
## <a name="remarks"></a>Remarques

Les chaînes de modèle de format sont utilisées par la fonction FORMAT pour définir le développement des valeurs en dates, heures, nombres et intitulés d’unité.
  
## <a name="example"></a>Exemple

FIELDPICTURE(0)
  
Renvoie la chaîne de modèle de format « esc(0) », qui permet de représenter un nombre à une décimale dont l’unité est en minuscule lorsque la fonction FORMAT est utilisée.
  