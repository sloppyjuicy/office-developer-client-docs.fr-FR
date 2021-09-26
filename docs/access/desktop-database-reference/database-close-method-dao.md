---
title: Database.Close, méthode (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5676ad0289891fad442e5670fc0d3d9c8d769419
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618265"
---
# <a name="databaseclose-method-dao"></a>Database.Close, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Ferme un objet **Database** ouvert.

## <a name="syntax"></a>Syntaxe

*expression* .Close

*expression* Variable qui représente un objet **Database**.

## <a name="remarks"></a>Remarques

Si l'objet **Database** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.

Une alternative à l’utilisation de la méthode **Close** consiste à définir la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).

