---
title: Server, propriété (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 062a4a319073ccf8f2810205973c11a845e2cc6f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925232"
---
# <a name="server-property-rds"></a>Server, propriété (RDS)


**S’applique à**: Access 2013, Office 2013

Indique le nom de l'IIS (Internet Information Services) et du protocole de communication.

Vous pouvez définir la propriété **Server** à la conception dans les balises OBJECT de l'objet [RDS.DataControl](datacontrol-object-rds.md) ou à l'exécution dans le code de script.

## <a name="syntax"></a>Syntaxe

|Protocole|Syntaxe à la conception|
|:-------|:-----------------|
|HTTP|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|HTTPS|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|DCOM|`<PARAM NAME="Server" VALUE="computername">`|
|In-process|`<PARAM NAME="Server" VALUE="">`|


|Protocole|Syntaxe à l'exécution|
|:-------|:--------------|
|HTTP|`DataControl.Server="https://awebsrvr:port"`|
|HTTPS|`DataControl.Server="https://awebsrvr:port"`|
|DCOM|`DataControl.Server="computername"`|
|In-process|`DataControl.Server=""`|


## <a name="parameters"></a>Paramètres

*awebsrvr* ou *computername*

- Une valeur **String** qui contient un chemin d'accès Internet ou intranet, un nom d'ordinateur (si le serveur se trouve sur un ordinateur distant) ou une chaîne vide si le serveur se trouve sur l'ordinateur local.

*port*

- Facultatif. Un port utilisé pour se connecter à un serveur IIS. Le numéro du port est défini dans Internet Explorer (dans le menu **Outils**, cliquez sur **Options Internet** et sélectionnez l'onglet **Connexion** ) ou dans IIS.

*DataControl*

- Une variable objet qui représente un objet **RDS.DataControl**.

## <a name="remarks"></a>Remarques

Le serveur est l'endroit où la requête **RDS.DataControl** (une demande ou une mise à jour) est traitée. Par défaut, toutes les requêtes sont traitées par l'objet [RDSServer.DataFactory](datafactory-object-rdsserver.md), le composant [MSDFMAP.Handler](datafactory-customization.md) et le fichier [MSDFMAP.INI](understanding-the-customization-file.md) sur le serveur spécifié. 

Souvenez-vous, lorsque vous changez de serveur, de comparer les paramètres des anciens et des nouveaux fichiers **MSDFMAP.INI**. S'ils ne sont pas compatibles, les requêtes qui aboutissent sur un serveur peuvent générer des erreurs sur un autre. Si la valeur de la propriété Server est « », ces objets seront utilisés sur la machine locale.

