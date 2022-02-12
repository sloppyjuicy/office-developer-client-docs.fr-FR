---
title: STRSAMEEX, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
ms.localizationpriority: medium
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Détermine si deux chaînes sont identiques.
ms.openlocfilehash: d2656ee2912467a6a879da3244d61c3c80c16488
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773837"
---
# <a name="strsameex-function"></a>Fonction STRSAMEEX

Détermine si deux chaînes sont identiques.
  
## <a name="syntax"></a>Syntaxe

STRSAMEEX ( » ***string1** _ « , " _*_string2_*_ « , _*_localeID_*_, _ *_flag_** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Requis  <br/> |**String** <br/> |Première chaîne à comparer. |
| _string2_ <br/> |Requis  <br/> |**String** <br/> | Deuxième chaîne à comparer. |
| _localeID_ <br/> |Requis  <br/> |**Numérique** <br/> |Code du pays (paramètre régional). |
| _flag_ <br/> |Requis  <br/> |**Numérique** <br/> | Bit qui indique le type de comparaison. |
   
### <a name="return-value"></a>Valeur renvoyée

Booléen
  
## <a name="remarks"></a>Remarques

STRSAMEEX renvoie TRUE si les deux chaînes d’entrée sont identiques et FALSE dans le cas contraire. Utilisez cette fonction pour comparer des chaînes multi-octets ou pour effectuer des comparaisons qui font appel à des règles de casse pour un paramètre régional spécifique.
			

  
Vous pouvez utiliser toute combinaison des indicateurs suivants avec la fonction STRSAMEEX.
  
|**Indicateur**|**Description**|
|:-----|:-----|
|1  <br/> |Ne tient pas compte de la casse. |
|2  <br/> |Ne tient pas compte des caractères qui ne définissent pas d’espacement. |
|4  <br/> |Ne tient pas compte des symboles. |
|4096  <br/> |Traite les signes de ponctuation comme des symboles. |
|65536  <br/> |Ne fait aucune différence entre les caractères Hiragana et Katakana. |
|131072  <br/> |Ne fait aucune différence entre un caractère codé sur un octet et le même caractère codé sur deux octets. |
   

