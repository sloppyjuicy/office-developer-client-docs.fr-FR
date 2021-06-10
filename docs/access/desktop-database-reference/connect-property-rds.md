---
title: Connecter propriété (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295981"
---
# <a name="connect-property-rds"></a>Connecter propriété (RDS)

**S’applique à** : Access 2013, Office 2013

Indique le nom de la base de données dans laquelle les opérations de requête et de mise à jour sont exécutées.

Vous pouvez définir la propriété **Connect** au moment du design dans les balises OBJECT de l’objet [RDS.DataControl](datacontrol-object-rds.md) ou au moment de l’exécution dans le code de script (par exemple, VBScript).

## <a name="syntax"></a>Syntaxe

Moment de la conception \< : PARAM NAME="Connecter » VALUE="ConnectionString »\>

Durée d’application : DataControl. Connecter = « ConnectionString »

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ConnectionString* |Chaîne de connexion valide. Pour plus d'informations d'ordre général sur les chaînes de connexion, reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md) ou à la documentation du fournisseur.<br/><br/>**REMARQUE**: spécifier MS Remote comme fournisseur pour **rdS. DataControl** créerait un scénario à quatre niveaux. Les scénarios comptant plus de trois niveaux n'ont pas été testés et sont normalement inutiles.|
|*DataControl* |Une variable objet qui représente un objet **RDS.DataControl**.|

