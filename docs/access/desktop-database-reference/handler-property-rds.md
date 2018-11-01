---
title: Handler, propriété (RDS)
TOCTitle: Handler Property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcb0b7f635e9ad74e6d8733a2f0fbe0153ac4739
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884869"
---
# <a name="handler-property-rds"></a>Handler, propriété (RDS)


**S’applique à**: Access 2013, Office 2013


Indique le nom d’un programme de personnalisation coté serveur (gestionnaire) qui étend la fonctionnalité de [RDSServer.DataFactory](datafactory-object-rdsserver.md) et tous les paramètres utilisés par le *gestionnaire (handler)*.

## <a name="syntax"></a>Syntaxe

*DataControl*. Gestionnaire = *chaîne*

## <a name="parameters"></a>Paramètres

  - *DataControl*

  - Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).

  - *String*

  - Une valeur de **type String** qui contient le nom du gestionnaire et des paramètres, séparés par des virgules (par exemple, « handlerName, parm1, parm2,..., parm *N*»).

## <a name="remarks"></a>Remarques

Cette propriété prend en charge la personnalisation, fonctionnalité pour laquelle il faut donner à la propriété [CursorLocation](cursorlocation-property-ado.md) la valeur **adUseClient**.

Les noms du gestionnaire et de ses paramètres, le cas échéant, sont séparés par des virgules (« , »). Le comportement n'est pas garanti si un point-virgule (« ; ») apparaît dans la valeur *String*. Vous pouvez écrire votre propre gestionnaire à condition qu'il prenne en charge l'interface **IDataFactoryHandler**.

Le gestionnaire par défaut s'appelle **MSDFMAP.Handler**, son paramètre par défaut est un fichier de personnalisation appelé **MSDFMAP.INI**. Utilisez cette propriété pour appeler les autres fichiers de personnalisation créés par votre administrateur serveur.

Définir la propriété **Handler** consiste à spécifier un gestionnaire et des paramètres dans la propriété [ConnectionString](connectionstring-property-ado.md) . Autrement dit, « **Gestionnaire = *** handlerName, parm1, parm2,... ;*».

