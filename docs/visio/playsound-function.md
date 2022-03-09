---
title: PLAYSOUND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
ms.localizationpriority: medium
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: Lit un fichier audio ou un son système.
ms.openlocfilehash: 26e26f89b28436e23cc430842c1ace69c7cfdca8
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404186"
---
# <a name="playsound-function"></a>Fonction PLAYSOUND

Lit un fichier audio ou un son système.
  
## <a name="syntax"></a>Syntaxe

PLAYSOUND( » ***filename** _ « | » _*_alias_*_ « , _*_isAlias_*_, _*_beep_*_, _ *_synch_** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *filename* <br/> |Requis  <br/> |**String** <br/> |Nom du fichier audio à lire. |
| *alias* <br/> |Requis  <br/> |**String** <br/> | Son système représenté par un alias. |
| *isAlias* <br/> |Obligatoire  <br/> |**Booléen** <br/> | Indique si l’expression précédente est un alias ou un nom de fichier ; une valeur non nulle est un alias. |
| *beep* <br/> |Obligatoire  <br/> |**Booléen** <br/> |Microsoft Visio émet un signal sonore s’il n’arrive pas à lire le son ; une valeur non nulle active le signal sonore. |
| *synch* <br/> |Obligatoire  <br/> |**Booléen** <br/> |Détermine si les sons sont lus de manière asynchrone (0) ou synchrone (1). |

## <a name="remarks"></a>Remarques

Vous devez généralement lire les sons de manière asynchrone pour que Visio puisse poursuivre le traitement pendant la lecture du son. Pour enchaîner plusieurs sons ensemble, lisez-les de manière synchrone afin d’éviter les échecs de lecture.

  
## <a name="example-1"></a>Exemple 1

PLAYSOUND("piano.wav"; 0; 0; 0)
  
Émet le fichier audio piano.wav de façon asynchrone et sans signal d’avertissement en cas d’échec.
  
## <a name="example-2"></a>Exemple 2

PLAYSOUND("SystemExclamation"; 1; 0; 0)
  
Émet le son système d’exclamation de façon asynchrone et sans signal d’avertissement en cas d’échec.
  