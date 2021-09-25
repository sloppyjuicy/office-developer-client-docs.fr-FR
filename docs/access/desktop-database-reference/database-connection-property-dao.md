---
title: Database.Connection, propriété (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4bf01881184347f5a9d1f36cb0c4b997fb5baf38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585948"
---
# <a name="databaseconnection-property-dao"></a>Database.Connection, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*.* Connexion

*expression* Variable qui représente un objet **Database**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Connection** pour obtenir une référence à un objet **Connection** correspondant à l'objet **Database**. Dans DAO, un objet **Connection** et l'objet **Database** correspondant représentent deux références de variable d'objet différentes au même objet. Grâce à la propriété **[Database](connection-database-property-dao.md)** d'un objet **Connection** et à la propriété **Connection** d'un objet **Database**, il est plus simple de modifier la connexion à une source de données ODBC via le moteur de base de données Microsoft Access afin d'utiliser ODBCDirect.

