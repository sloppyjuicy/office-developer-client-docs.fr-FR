---
title: PLAYSOUND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: Lit un fichier audio ou un son système.
ms.openlocfilehash: ca54b749b764e9ea2c7db71d41268303542417f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789276"
---
# <a name="playsound-function"></a>PLAYSOUND, fonction

Lit un fichier audio ou un son système. 
  
## <a name="syntax"></a>Syntaxe

PLAYSOUND (« ** *filename* ** « | » ** *alias* ** », ** *estAlias* **, ** *Bip* **, ** *synch* **) 
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _nom de fichier_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> |Nom du fichier audio à lire.  <br/> |
| _alias_ <br/> |Obligatoire  <br/> |**Chaîne** <br/> | Son système représenté par un alias.  <br/> |
| _estAlias_ <br/> |Obligatoire  <br/> |**Boolean** <br/> | Indique si l’expression précédente est un alias ou un nom de fichier ; une valeur non nulle est un alias.  <br/> |
| _bip_ <br/> |Obligatoire  <br/> |**Boolean** <br/> |Microsoft Visio émet un signal sonore s’il n’arrive pas à lire le son ; une valeur non nulle active le signal sonore.  <br/> |
| _synchronisation_ <br/> |Obligatoire  <br/> |**Boolean** <br/> |Détermine si les sons sont lus de manière asynchrone (0) ou synchrone (1).  <br/> |
   
## <a name="remarks"></a>Note

Vous devez généralement lire les sons asynchrone afin que Visio peut continuer à traiter pendant qu’il lit le son. Pour enchaîner plusieurs sons ensemble, les lire de façon synchrone ou certains ne parvient pas à lire. 
  
## <a name="example-1"></a>Exemple 1

PLAYSOUND("piano.wav"; 0; 0; 0)
  
Émet le fichier audio piano.wav de façon asynchrone et sans signal d’avertissement en cas d’échec.
  
## <a name="example-2"></a>Exemple 2

PLAYSOUND("SystemExclamation"; 1; 0; 0)
  
Émet le son système d’exclamation de façon asynchrone et sans signal d’avertissement en cas d’échec.
  

