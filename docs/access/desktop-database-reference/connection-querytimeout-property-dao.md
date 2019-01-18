---
title: Propriété Connection.QueryTimeout (DAO)
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
localization_priority: Normal
ms.openlocfilehash: a2a03b97fc69d6d770a5d7a1d149f6518933002b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711090"
---
# <a name="connectionquerytimeout-property-dao"></a>Propriété Connection.QueryTimeout (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou retourne une valeur qui spécifie le nombre de secondes d'attente avant qu'une erreur de délai d'attente soit générée lors de l'exécution d'une requête sur une source de données ODBC.

## <a name="syntax"></a>Syntaxe

*expression* . QueryTimeout

*expression* Variable qui représente un objet **Connection** .

## <a name="remarks"></a>Remarques

La valeur par défaut est 60.

Lorsque vous utilisez une base de données ODBC, telle que Microsoft SQL Server, le trafic réseau ou une utilisation intensive du serveur ODBC peut entraîner des délais. Au lieu d'attendre indéfiniment, vous pouvez définir le délai d'attente.

Lorsque vous utilisez **QueryTimeout** avec un objet **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)**, cette propriété spécifie une valeur globale pour toutes les requêtes associées à la base de données. Vous pouvez remplacer cette valeur pour une requête donnée en définissant la propriété **ODBCTimeout** de l'objet **[QueryDef](querydef-object-dao.md)** concerné.

