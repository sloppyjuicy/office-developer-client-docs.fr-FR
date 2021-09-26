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
ms.openlocfilehash: 7dab11245389c02054b5f3d626334867dcbad437
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627715"
---
# <a name="playsound-function"></a>Fonction PLAYSOUND

Lit un fichier audio ou un son système. 
  
## <a name="syntax"></a>Syntaxe

PLAYSOUND( » ** *filename* ** « | » ** *alias* ** « , ** *isAlias* **, ** *beep* **, ** *synch* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _filename_ <br/> |Obligatoire  <br/> |**String** <br/> |Nom du fichier audio à lire.  <br/> |
| _alias_ <br/> |Obligatoire  <br/> |**String** <br/> | Son système représenté par un alias.  <br/> |
| _isAlias_ <br/> |Obligatoire  <br/> |**Booléen** <br/> | Indique si l’expression précédente est un alias ou un nom de fichier ; une valeur non nulle est un alias.  <br/> |
| _beep_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Microsoft Visio émet un signal sonore s’il n’arrive pas à lire le son ; une valeur non nulle active le signal sonore.  <br/> |
| _synch_ <br/> |Obligatoire  <br/> |**Booléen** <br/> |Détermine si les sons sont lus de manière asynchrone (0) ou synchrone (1).  <br/> |
   
## <a name="remarks"></a>Remarques

Vous devez généralement lire les sons de manière asynchrone pour que Visio puisse poursuivre le traitement pendant la lecture du son. Pour enchaîner plusieurs sons ensemble, lisez-les de manière synchrone afin d’éviter les échecs de lecture.
 
  
## <a name="example-1"></a>Exemple 1

PLAYSOUND("piano.wav"; 0; 0; 0)
  
Émet le fichier audio piano.wav de façon asynchrone et sans signal d’avertissement en cas d’échec.
  
## <a name="example-2"></a>Exemple 2

PLAYSOUND("SystemExclamation"; 1; 0; 0)
  
Émet le son système d’exclamation de façon asynchrone et sans signal d’avertissement en cas d’échec.
  

