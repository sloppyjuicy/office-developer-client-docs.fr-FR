---
title: LISTSEP, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251882
localization_priority: Normal
ms.assetid: 73dc5981-2c8c-e76e-e4bd-e65a7c8db242
description: Renvoie la chaîne de séparateur de liste pour les paramètres régionaux de l’utilisateur actuel.
ms.openlocfilehash: 901442a3c2af8509855b8b038057e7f813634ea1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431406"
---
# <a name="listsep-function"></a>Fonction LISTSEP

Renvoie la chaîne de séparateur de liste pour les paramètres régionaux de l’utilisateur actuel.
  
## <a name="syntax"></a>Syntaxe

LISTSEP ()
  
### <a name="return-value"></a>Valeur renvoyée

String
  
## <a name="example"></a>Exemple

SETF(GETREF(user.extent), « MAX(Width » &amp; ListSep() &amp; « Height) ») 
  

