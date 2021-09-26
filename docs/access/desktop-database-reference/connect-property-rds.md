---
title: Connecter propriété (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 49f62accab5a4da7d89c545bf82d0593238be1c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597617"
---
# <a name="connect-property-rds"></a>Connecter propriété (RDS)

**S’applique à** : Access 2013, Office 2013

Indique le nom de la base de données dans laquelle les opérations de requête et de mise à jour sont exécutées.

Vous pouvez définir la propriété **Connect** au moment du design dans les balises OBJECT de l’objet [RDS.DataControl](datacontrol-object-rds.md) ou au moment de l’exécution dans le code de script (par exemple, VBScript).

## <a name="syntax"></a>Syntaxe

Moment de la conception : \<PARAM NAME="Connect" VALUE="ConnectionString"\>

Durée d’application : DataControl. Connecter = « ConnectionString »

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ConnectionString* |Chaîne de connexion valide. Pour plus d'informations d'ordre général sur les chaînes de connexion, reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md) ou à la documentation du fournisseur.<br/><br/>**REMARQUE**: spécifier MS Remote comme fournisseur pour **rdS. DataControl** créerait un scénario à quatre niveaux. Les scénarios comptant plus de trois niveaux n'ont pas été testés et sont normalement inutiles.|
|*DataControl* |Une variable objet qui représente un objet **RDS.DataControl**.|

