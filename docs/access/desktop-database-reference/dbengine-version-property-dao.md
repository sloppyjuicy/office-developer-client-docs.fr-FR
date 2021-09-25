---
title: DBEngine.Version, propriété (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: c55d0770001c4232327d55cd81d1bd40a435b73d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585773"
---
# <a name="dbengineversion-property-dao"></a>DBEngine.Version, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie la version de DAO en cours d'utilisation. Valeur de type **String** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* Version

*expression* Variable représentant un objet **DBEngine**.

## <a name="remarks"></a>Remarques

La valeur renvoyée est une chaîne (type String) correspondant à un numéro de version au format « principale.secondaire ». Par exemple, « 3.0 ». Le numéro de version du produit comprend le numéro de version principale (3), un point, puis le numéro de version secondaire (0).

