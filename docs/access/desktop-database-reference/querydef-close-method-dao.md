---
title: QueryDef.Close, méthode (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 98fb593324cdae9c8164ca40f19834500a83acb4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577030"
---
# <a name="querydefclose-method-dao"></a>QueryDef.Close, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Ferme un objet **QueryDef** ouvert.

## <a name="syntax"></a>Syntaxe

*expression* .Close

*expression* Variable représentant un objet **QueryDef**.

## <a name="remarks"></a>Remarques

Si l'objet **QueryDef** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.

Une alternative à l’utilisation de la méthode **Close** consiste à définir la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).

