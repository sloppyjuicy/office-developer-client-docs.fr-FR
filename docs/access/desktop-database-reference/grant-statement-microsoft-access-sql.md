---
title: GRANT, instruction (Microsoft Access SQL)
TOCTitle: GRANT statement (Microsoft Access SQL)
ms:assetid: 50ae97ae-d5be-57e5-d9da-f3fc42f01d83
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193820(v=office.15)
ms:contentKeyID: 48544800
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277478
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4357099f8bcb9b2308b5cda3543949765b8c3420
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292131"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="4bef5-102">GRANT, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4bef5-102">GRANT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="4bef5-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bef5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bef5-104">Accorde des privilèges spécifiques à un utilisateur ou un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="4bef5-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bef5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bef5-105">Syntax</span></span>

<span data-ttu-id="4bef5-106">GRANT {*privilège* \[ , *privilège*, ... \] } ON{Table *|* OBJECT, *objet*|</span><span class="sxs-lookup"><span data-stu-id="4bef5-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="4bef5-107">CONTAINER *container* } TO {*authorizationname* \[ , *authorizationname*, ... \] }</span><span class="sxs-lookup"><span data-stu-id="4bef5-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="4bef5-108">L'instruction GRANT est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4bef5-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bef5-109">Élément</span><span class="sxs-lookup"><span data-stu-id="4bef5-109">Part</span></span></p></th>
<th><p><span data-ttu-id="4bef5-110">Description</span><span class="sxs-lookup"><span data-stu-id="4bef5-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bef5-111"><em>privilège</em></span><span class="sxs-lookup"><span data-stu-id="4bef5-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="4bef5-112">Privilège à accorder.</span><span class="sxs-lookup"><span data-stu-id="4bef5-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="4bef5-113">Les privilèges sont spécifiés à l’aide des mots clés suivants : SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA et UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="4bef5-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bef5-114"><em>tablename</em></span><span class="sxs-lookup"><span data-stu-id="4bef5-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="4bef5-115">Tout nom de table valide.</span><span class="sxs-lookup"><span data-stu-id="4bef5-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bef5-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="4bef5-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="4bef5-117">Tout objet autre qu'une table.</span><span class="sxs-lookup"><span data-stu-id="4bef5-117">This can encompass any non-table object.</span></span> <span data-ttu-id="4bef5-118">Il peut s'agir d'une requête stockée (vue ou procédure), par exemple.</span><span class="sxs-lookup"><span data-stu-id="4bef5-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bef5-119"><em>conteneur</em></span><span class="sxs-lookup"><span data-stu-id="4bef5-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="4bef5-120">Nom d'un conteneur valide.</span><span class="sxs-lookup"><span data-stu-id="4bef5-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bef5-121"><em>authorizationname</em></span><span class="sxs-lookup"><span data-stu-id="4bef5-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="4bef5-122">Nom d'utilisateur ou de groupe.</span><span class="sxs-lookup"><span data-stu-id="4bef5-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

