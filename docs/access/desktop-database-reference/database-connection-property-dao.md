---
title: Propriété Database.Connection (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9aecffc135ab402f02b8fd4e1cc234f4a6eb37d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927325"
---
# <a name="databaseconnection-property-dao"></a>Propriété Database.Connection (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . Connexion

*expression* Variable qui représente un objet de **base de données** .

## <a name="remarks"></a>Remarques

Utilisez la propriété **Connection** pour obtenir une référence à un objet **Connection** correspondant à l'objet **Database**. Dans DAO, un objet **Connection** et l'objet **Database** correspondant représentent deux références de variable d'objet différentes au même objet. Grâce à la propriété **[Database](connection-database-property-dao.md)** d'un objet **Connection** et à la propriété **Connection** d'un objet **Database**, il est plus simple de modifier la connexion à une source de données ODBC via le moteur de base de données Microsoft Access afin d'utiliser ODBCDirect.

