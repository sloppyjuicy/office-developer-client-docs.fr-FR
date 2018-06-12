---
title: STRSAMEEX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Détermine si les deux chaînes sont identiques.
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789835"
---
# <a name="strsameex-function"></a>STRSAMEEX, fonction

Détermine si les deux chaînes sont identiques.
  
## <a name="syntax"></a>Syntaxe

STRSAMEEX (« ** *chaîne1* ** «, » ** *chaîne2* ** », ** *localeID* **, ** *indicateur* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _chaîne string1_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Première chaîne à comparer.  <br/> |
| _chaîne2_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Deuxième chaîne à comparer.  <br/> |
| _localeID_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Code du pays (paramètre régional).  <br/> |
| _indicateur_ <br/> |Obligatoire  <br/> |**Numérique** <br/> | Bit qui indique le type de comparaison.  <br/> |
   
### <a name="return-value"></a>Valeur renvoy�e

Booléenne
  
## <a name="remarks"></a>Remarques

STRSAMEEX renvoie TRUE si les deux chaînes d’entrée sont identiques et FALSE si elles ne sont pas. Utilisez cette fonction pour comparer des chaînes multi-octets ou pour effectuer des comparaisons qui utilisent des règles de casse pour un paramètre régional spécifique.
  
Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction STRSAMEEX.
  
|**Indicateur**|**Description**|
|:-----|:-----|
|1  <br/> |Ne tient pas compte de la casse.  <br/> |
|2  <br/> |Ne tient pas compte des caractères qui ne définissent pas d’espacement.  <br/> |
|4  <br/> |Ne tient pas compte des symboles.  <br/> |
|4096  <br/> |Traite les signes de ponctuation comme des symboles.  <br/> |
|65536  <br/> |Ne fait aucune différence entre les caractères Hiragana et Katakana.  <br/> |
|131072  <br/> |Ne fait aucune différence entre un caractère codé sur un octet et le même caractère codé sur deux octets.  <br/> |
   

