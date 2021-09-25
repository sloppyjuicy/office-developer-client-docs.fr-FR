---
title: State, propriété (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 311c21d628a77d3835ef40c849385e9946fd79dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617397"
---
# <a name="state-property-ado"></a>State, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique, pour tous les objets applicables, si l'état de l'objet est ouvert ou fermé.

Indique, pour tous les objets applicables exécutant une méthode asynchrone, si l'état actuel de l'objet est « en cours de connexion », « en cours d'exécution » ou « en cours d'extraction ».

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Long** pouvant être une valeur [ObjectStateEnum](objectstateenum.md). La valeur par défaut est **adStateClosed**.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser à tout moment la propriété **State** pour déterminer l'état actuel d'un objet donné.

La propriété **State** de l'objet peut présenter plusieurs valeurs associées. Par exemple, si une instruction est en cours d'exécution, cette propriété aura la valeur **adStateOpen** associée à **adStateExecuting**.

La propriété **State** est en lecture seule.

