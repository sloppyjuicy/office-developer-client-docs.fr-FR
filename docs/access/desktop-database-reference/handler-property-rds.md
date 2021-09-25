---
title: Propriété Handler (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1ea6d8a4ba0bb4a2b9a5a61e8241e853408b6263
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594208"
---
# <a name="handler-property-rds"></a>Propriété Handler (RDS)

**S’applique à** : Access 2013, Office 2013

Indique le nom d’un programme de personnalisation coté serveur (gestionnaire) qui étend la fonctionnalité de [RDSServer.DataFactory](datafactory-object-rdsserver.md) et tous les paramètres utilisés par le *gestionnaire (handler)*.

## <a name="syntax"></a>Syntaxe

*DataControl*. Handler = *String*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*DataControl* |Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Valeur **de** chaîne qui contient le nom du handler et tous les paramètres, séparés par des virgules (par exemple, « handlerName,parm1,parm2,...,parm *N*».|

## <a name="remarks"></a>Remarques

Cette propriété prend en charge la personnalisation, fonctionnalité pour laquelle il faut donner à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**.

Les noms du gestionnaire et de ses paramètres, le cas échéant, sont séparés par des virgules (« , »). Le comportement n'est pas garanti si un point-virgule (« ; ») apparaît dans la valeur *String*. Vous pouvez écrire votre propre gestionnaire à condition qu'il prenne en charge l'interface **IDataFactoryHandler**.

Le gestionnaire par défaut s'appelle **MSDFMAP.Handler**, son paramètre par défaut est un fichier de personnalisation appelé **MSDFMAP.INI**. Utilisez cette propriété pour appeler les autres fichiers de personnalisation créés par votre administrateur serveur.

Si vous ne souhaitez pas définir la propriété **Handler**, vous pouvez spécifier un gestionnaire et des paramètres dans la propriété [ConnectionString](connectionstring-property-ado.md) : « **Handler=**_handlerName,parm1,parm2,...;_  ».

