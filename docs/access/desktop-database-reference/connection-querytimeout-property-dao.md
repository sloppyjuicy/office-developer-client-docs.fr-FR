---
title: Connection.QueryTimeout, propriété (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: 97853412-d5ae-7a71-ccaa-595c68919654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197804(v=office.15)
ms:contentKeyID: 48546471
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052905
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 6a7c98fb9b5c64f7db657f9a2c12c07688b50fcb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615759"
---
# <a name="connectionquerytimeout-property-dao"></a>Connection.QueryTimeout, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou retourne une valeur qui spécifie le nombre de secondes d’attente avant qu’une erreur de délai d’attente soit générée lors de l’exécution d’une requête sur une source de données ODBC.

## <a name="syntax"></a>Syntaxe

*.* QueryTimeout

*expression* Variable qui représente un objet **Connection**.

## <a name="remarks"></a>Remarques

La valeur par défaut est 60.

En cas d'utilisation d'une base de données ODBC, comme Microsoft SQL Server, vous pouvez subir des retards dus au trafic du réseau ou à l'utilisation intensive du serveur ODBC. Au lieu d'attendre indéfiniment, vous pouvez déterminer la durée d'attente.

Lorsque vous utilisez **QueryTimeout** avec un objet **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)**, cette propriété spécifie une valeur globale pour toutes les requêtes associées à la base de données. Vous pouvez remplacer cette valeur pour une requête donnée en définissant la propriété **ODBCTimeout** de l'objet **[QueryDef](querydef-object-dao.md)** concerné.

