---
title: DECIMALSEP, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
ms.localizationpriority: medium
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: Renvoie la chaîne de séparateur décimal pour les paramètres régionaux de l’utilisateur actuel.
ms.openlocfilehash: 6f4262aa649d96514d5a0939f464d99404cce9d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594628"
---
# <a name="decimalsep-function"></a>Fonction DECIMALSEP

Renvoie la chaîne de séparateur décimal pour les paramètres régionaux de l’utilisateur actuel.
  
## <a name="syntax"></a>Syntaxe

DECIMALSEP( )
  
## <a name="example"></a>Exemple

SETF(GETREF(user.size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart) 
  

