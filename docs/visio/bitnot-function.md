---
title: BITNOT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
ms.localizationpriority: medium
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 uniquement si le bit correspondant dans le nombre binaire est 0. Dans le cas contraire, le bit est définie sur 0.
ms.openlocfilehash: 7b9c6c76315dd4dbe64b8edbd4f40bc8d84ecfe8
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63404361"
---
# <a name="bitnot-function"></a>Fonction BITNOT

Renvoie un nombre binaire 16 bits dans lequel chaque bit est définie sur 1 uniquement si le bit correspondant dans le nombre binaire est 0. Dans le cas contraire, le bit est définie sur 0.
  
## <a name="syntax"></a>Syntaxe

BITNOT(***binary number*** )
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| *nombre binaire* <br/> |Requis  <br/> |**Numérique** <br/> |Nombre binaire de 16 bits. |

### <a name="return-value"></a>Valeur renvoyée

Binaire de 16 bits
  
## <a name="example"></a>Exemple

BITNOT(6)
  
Renvoie 65529. Le 6 = 0...00110. Donc, BITNOT(6) = 1...11001.
  