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
description: Détermine si deux chaînes sont identiques.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413863"
---
# <a name="strsameex-function"></a>Fonction STRSAMEEX

Détermine si deux chaînes sont identiques.
  
## <a name="syntax"></a>Syntaxe

STRSAMEEX ("* * *Chaîne1* * *", "* * *Chaîne2* * *", * * *LocaleID* * *, * * *indicateur* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Obligatoire  <br/> |**String** <br/> |Première chaîne à comparer.  <br/> |
| _string2_ <br/> |Obligatoire  <br/> |**String** <br/> | Deuxième chaîne à comparer.  <br/> |
| _Régionaux_ <br/> |Obligatoire  <br/> |**Numérique** <br/> |Code du pays (paramètre régional).  <br/> |
| _indicateur_ <br/> |Obligatoire  <br/> |**Numérique** <br/> | Bit qui indique le type de comparaison.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="remarks"></a>Remarques

STRSAMEEX renvoie TRUE si les deux chaînes d’entrée sont identiques et FALSE dans le cas contraire. Utilisez cette fonction pour comparer des chaînes multi-octets ou pour effectuer des comparaisons qui font appel à des règles de casse pour un paramètre régional spécifique.
  
Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction STRSAMEEX.
  
|**Indicateur**|**Description**|
|:-----|:-----|
|0,1  <br/> |Ne tient pas compte de la casse.  <br/> |
|n°2  <br/> |Ne tient pas compte des caractères qui ne définissent pas d’espacement.  <br/> |
|4  <br/> |Ne tient pas compte des symboles.  <br/> |
|4096  <br/> |Traite les signes de ponctuation comme des symboles.  <br/> |
|65536  <br/> |Ne fait aucune différence entre les caractères Hiragana et Katakana.  <br/> |
|131072  <br/> |Ne fait aucune différence entre un caractère codé sur un octet et le même caractère codé sur deux octets.  <br/> |
   

