---
title: Propriété Database. Connection (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77d9bfa30dbfab21fd75de36b336a25e6af3187e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294994"
---
# <a name="databaseconnection-property-dao"></a>Propriété Database. Connection (DAO)


**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . Connexion

*expression* Variable qui représente un objet **Database** .

## <a name="remarks"></a>Remarques

Utilisez la propriété **Connection** pour obtenir une référence à un objet **Connection** correspondant à l'objet **Database**. Dans DAO, un objet **Connection** et l'objet **Database** correspondant représentent deux références de variable d'objet différentes au même objet. Grâce à la propriété **[Database](connection-database-property-dao.md)** d'un objet **Connection** et à la propriété **Connection** d'un objet **Database**, il est plus simple de modifier la connexion à une source de données ODBC via le moteur de base de données Microsoft Access afin d'utiliser ODBCDirect.

