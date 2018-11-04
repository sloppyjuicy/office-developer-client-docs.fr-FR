---
title: Connect, propriété (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b0d0969d9cbcf972a1b57faf27bbea1dfd960d5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949417"
---
# <a name="connect-property-rds"></a>Connect, propriété (RDS)

**S’applique à**: Access 2013, Office 2013

Indique le nom de la base de données dans laquelle les opérations de requête et de mise à jour sont exécutées.

Vous pouvez définir la propriété **Connect** au moment du design dans les balises OBJECT de l'objet [RDS.DataControl](datacontrol-object-rds.md) ou au moment de l'exécution dans le code de script (par exemple, VBScript).

## <a name="syntax"></a>Syntaxe

Au moment du design : \<PARAM NAME = « Connexion », valeur = « ConnectionString »\>

Temps d’exécution : DataControl.Connect = « ConnectionString »

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ConnectionString* |Chaîne de connexion valide. Pour plus d'informations d'ordre général sur les chaînes de connexion, reportez-vous à la propriété [ConnectionString](connectionstring-property-ado.md) ou à la documentation du fournisseur.<br/><br/>**Remarque**: spécification MS Remote comme fournisseur pour le **RDS. DataControl** crée un scénario à quatre niveaux. Les scénarios comptant plus de trois niveaux n'ont pas été testés et sont normalement inutiles.|
|*DataControl* |Une variable objet qui représente un objet **RDS.DataControl**.|

