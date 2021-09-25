---
title: LISTSEP, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251882
ms.localizationpriority: medium
ms.assetid: 73dc5981-2c8c-e76e-e4bd-e65a7c8db242
description: Renvoie la chaîne de séparateur de liste pour les paramètres régionaux de l’utilisateur actuel.
ms.openlocfilehash: 5538d8e101ceffe86d33cd4a2e334789203840bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574005"
---
# <a name="listsep-function"></a>Fonction LISTSEP

Renvoie la chaîne de séparateur de liste pour les paramètres régionaux de l’utilisateur actuel.
  
## <a name="syntax"></a>Syntaxe

LISTSEP ()
  
### <a name="return-value"></a>Valeur renvoyée

String
  
## <a name="example"></a>Exemple

SETF(GETREF(user.extent), « MAX(Width » &amp; ListSep() &amp; « Height) ») 
  

