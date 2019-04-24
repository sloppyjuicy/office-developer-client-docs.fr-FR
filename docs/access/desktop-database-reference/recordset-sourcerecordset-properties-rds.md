---
title: Recordset, SourceRecordset, propriétés (RDS)
TOCTitle: Recordset, SourceRecordset properties (RDS)
ms:assetid: 5f4bb72d-ddfa-41c0-c353-b3a6632b4a91
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249345(v=office.15)
ms:contentKeyID: 48545160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f83ab385b1fab511ab71ea9ff3456fe466efa17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307587"
---
# <a name="recordset-sourcerecordset-properties-rds"></a>Recordset, SourceRecordset, propriétés (RDS)

**S’applique à** : Access 2013, Office 2013

Indique l’objet **Recordset** retourné d’un objet métier personnalisé.

## <a name="syntax"></a>Syntaxe

*DataControl*. SourceRecordset = *Recordset*

*Jeu d'enregistrements* = *DataControl*. Recordset

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*DataControl* |Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).|
|*Recordset* |Variable objet représentant un objet **Recordset**.|

## <a name="remarks"></a>Remarques

Vous pouvez donner comme valeur à la propriété **SourceRecordset** un [Recordset](recordset-object-ado.md) renvoyé par un objet métier personnalisé.

Ces propriétés permettent à une application de gérer le processus de liaison au moyen d'un processus personnalisé. Elles reçoivent un ensemble de lignes inséré dans un **Recordset**, pour que vous puissiez agir directement sur le **Recordset** (définition de propriétés ou itérations dans le **Recordset** ).

Vous pouvez définir la propriété **SourceRecordset** ou lire la propriété **Recordset** en mode exécution dans le code de script.

**SourceRecordset** est une propriété en écriture seule, contrairement à la propriété **Recordset** qui est en lecture seule.

