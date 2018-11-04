---
title: Query, méthode (RDS - référence du bureau de la base de données Access)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1e7f9dfc3ce5cb0d757951f13c1078ab44d04760
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949424"
---
# <a name="query-method-rds"></a><span data-ttu-id="89978-102">Query, méthode (RDS)</span><span class="sxs-lookup"><span data-stu-id="89978-102">Query method (RDS)</span></span>

<span data-ttu-id="89978-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89978-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89978-104">Utilise une chaîne de requête SQL valide qui retourne un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="89978-104">Uses a valid SQL query string to return a [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="89978-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89978-105">Syntax</span></span>

<span data-ttu-id="89978-106">Définir le*jeu d’enregistrements* = *DataFactory*. Requête (*connexion*, *requête*)</span><span class="sxs-lookup"><span data-stu-id="89978-106">Set*Recordset* = *DataFactory*.Query(*Connection*, *Query*)</span></span>

## <a name="parameters"></a><span data-ttu-id="89978-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89978-107">Parameters</span></span>

|<span data-ttu-id="89978-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="89978-108">Parameter</span></span>|<span data-ttu-id="89978-109">Description</span><span class="sxs-lookup"><span data-stu-id="89978-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="89978-110">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="89978-110">*Recordset*</span></span> |<span data-ttu-id="89978-111">Une variable objet qui représente un objet **Recordset**</span><span class="sxs-lookup"><span data-stu-id="89978-111">An object variable that represents a **Recordset** object.</span></span>|
|<span data-ttu-id="89978-112">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="89978-112">*DataFactory*</span></span> |<span data-ttu-id="89978-113">Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span><span class="sxs-lookup"><span data-stu-id="89978-113">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="89978-114">*Connexion*</span><span class="sxs-lookup"><span data-stu-id="89978-114">*Connection*</span></span> |<span data-ttu-id="89978-p101">Valeur de type **String** qui contient les informations de connexion de serveur. Ce paramètre est similaire à la propriété [Connect](connect-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="89978-p101">A **String** value that contains the server connection information. This is similar to the [Connect](connect-property-rds.md) property.</span></span>|
|<span data-ttu-id="89978-117">*Requête*</span><span class="sxs-lookup"><span data-stu-id="89978-117">*Query*</span></span> |<span data-ttu-id="89978-118">Valeur de type **String** qui contient la requête SQL.</span><span class="sxs-lookup"><span data-stu-id="89978-118">A **String** that contains the SQL query.</span></span>|

## <a name="remarks"></a><span data-ttu-id="89978-119">Notes</span><span class="sxs-lookup"><span data-stu-id="89978-119">Remarks</span></span>

<span data-ttu-id="89978-p102">La requête doit utiliser le langage SQL du serveur de base de données. Un état de résultat est retourné en cas d'erreur liée à la requête exécutée. La méthode **Query** ne procède à aucun vérification syntaxique de la chaîne du paramètre **Requête**.</span><span class="sxs-lookup"><span data-stu-id="89978-p102">The query should use the SQL dialect of the database server. A result status is returned if there is an error with the query that was executed. The **Query** method doesn't perform any syntax checking on the **Query** string.</span></span>

