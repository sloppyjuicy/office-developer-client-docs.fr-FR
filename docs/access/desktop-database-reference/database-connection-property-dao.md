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
# <a name="databaseconnection-property-dao"></a><span data-ttu-id="4e247-102">Propriété Database. Connection (DAO)</span><span class="sxs-lookup"><span data-stu-id="4e247-102">Database.Connection property (DAO)</span></span>


<span data-ttu-id="4e247-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e247-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="4e247-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e247-104">Syntax</span></span>

<span data-ttu-id="4e247-105">*expression* . Connexion</span><span class="sxs-lookup"><span data-stu-id="4e247-105">*expression* .Connection</span></span>

<span data-ttu-id="4e247-106">*expression* Variable qui représente un objet **Database** .</span><span class="sxs-lookup"><span data-stu-id="4e247-106">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e247-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e247-107">Remarks</span></span>

<span data-ttu-id="4e247-p101">Utilisez la propriété **Connection** pour obtenir une référence à un objet **Connection** correspondant à l'objet **Database**. Dans DAO, un objet **Connection** et l'objet **Database** correspondant représentent deux références de variable d'objet différentes au même objet. Grâce à la propriété **[Database](connection-database-property-dao.md)** d'un objet **Connection** et à la propriété **Connection** d'un objet **Database**, il est plus simple de modifier la connexion à une source de données ODBC via le moteur de base de données Microsoft Access afin d'utiliser ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="4e247-p101">Use the **Connection** property to obtain a reference to a **Connection** object that corresponds to the **Database**. In DAO, a **Connection** object and its corresponding **Database** object are simply two different object variable references to the same object. The **[Database](connection-database-property-dao.md)** property of a **Connection** object and the **Connection** property of a **Database** object make it easier to change connections to an ODBC data source through the Microsoft Access database engine to use ODBCDirect.</span></span>

