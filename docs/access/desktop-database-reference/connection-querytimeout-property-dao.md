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
# <a name="connectionquerytimeout-property-dao"></a><span data-ttu-id="2fffb-102">Propriété Connection.QueryTimeout (DAO)</span><span class="sxs-lookup"><span data-stu-id="2fffb-102">Connection.QueryTimeout property (DAO)</span></span>


<span data-ttu-id="2fffb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fffb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2fffb-104">Définit ou retourne une valeur qui spécifie le nombre de secondes d'attente avant qu'une erreur de délai d'attente soit générée lors de l'exécution d'une requête sur une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="2fffb-104">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fffb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fffb-105">Syntax</span></span>

<span data-ttu-id="2fffb-106">*expression* . QueryTimeout</span><span class="sxs-lookup"><span data-stu-id="2fffb-106">*expression* .QueryTimeout</span></span>

<span data-ttu-id="2fffb-107">*expression* Variable qui représente un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="2fffb-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fffb-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="2fffb-108">Remarks</span></span>

<span data-ttu-id="2fffb-109">La valeur par défaut est 60.</span><span class="sxs-lookup"><span data-stu-id="2fffb-109">The default value is 60.</span></span>

<span data-ttu-id="2fffb-p101">Lorsque vous utilisez une base de données ODBC, telle que Microsoft SQL Server, le trafic réseau ou une utilisation intensive du serveur ODBC peut entraîner des délais. Au lieu d'attendre indéfiniment, vous pouvez définir le délai d'attente.</span><span class="sxs-lookup"><span data-stu-id="2fffb-p101">When you're using an ODBC database, such as Microsoft SQL Server, there may be delays due to network traffic or heavy use of the ODBC server. Rather than waiting indefinitely, you can specify how long to wait.</span></span>

<span data-ttu-id="2fffb-p102">Lorsque vous utilisez **QueryTimeout** avec un objet **[Connection](connection-object-dao.md)** ou **[Database](database-object-dao.md)**, cette propriété spécifie une valeur globale pour toutes les requêtes associées à la base de données. Vous pouvez remplacer cette valeur pour une requête donnée en définissant la propriété **ODBCTimeout** de l'objet **[QueryDef](querydef-object-dao.md)** concerné.</span><span class="sxs-lookup"><span data-stu-id="2fffb-p102">When you use **QueryTimeout** with a **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object, it specifies a global value for all queries associated with the database. You can override this value for a specific query by setting the **ODBCTimeout** property of the particular **[QueryDef](querydef-object-dao.md)** object.</span></span>

