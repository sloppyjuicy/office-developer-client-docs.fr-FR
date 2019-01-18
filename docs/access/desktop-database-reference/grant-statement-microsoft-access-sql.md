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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716396"
---
# <a name="grant-statement-microsoft-access-sql"></a><span data-ttu-id="a53f2-102">GRANT, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="a53f2-102">GRANT statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="a53f2-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a53f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a53f2-104">Accorde des privilèges spécifiques à un utilisateur ou un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="a53f2-104">Grants specific privileges to an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="a53f2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a53f2-105">Syntax</span></span>

<span data-ttu-id="a53f2-106">GRANT {*privilège*\[, *privilège*, … \]} ON {TABLE *table* | OBJET, *objet*|</span><span class="sxs-lookup"><span data-stu-id="a53f2-106">GRANT {*privilege*\[, *privilege*, …\]} ON{TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="a53f2-107">CONTENEUR *conteneur* } TO {*nomautorisation*\[, *nomautorisation*, … \]}</span><span class="sxs-lookup"><span data-stu-id="a53f2-107">CONTAINER *container* } TO {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="a53f2-108">L'instruction GRANT est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a53f2-108">The GRANT statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a53f2-109">Argument</span><span class="sxs-lookup"><span data-stu-id="a53f2-109">Part</span></span></p></th>
<th><p><span data-ttu-id="a53f2-110">Description</span><span class="sxs-lookup"><span data-stu-id="a53f2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a53f2-111"><em>privilège</em></span><span class="sxs-lookup"><span data-stu-id="a53f2-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="a53f2-112">L’ou les privilèges à accorder.</span><span class="sxs-lookup"><span data-stu-id="a53f2-112">The privilege or privileges to be granted.</span></span> <span data-ttu-id="a53f2-113">Les privilèges sont spécifiés à l’aide de mots clés suivants : sélectionnez, DELETE, INSERT, UPDATE, dépôt, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA et UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="a53f2-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a53f2-114"><em>nomtable</em></span><span class="sxs-lookup"><span data-stu-id="a53f2-114"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="a53f2-115">Tout nom de table valide.</span><span class="sxs-lookup"><span data-stu-id="a53f2-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a53f2-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="a53f2-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="a53f2-p102">Tout objet autre qu'une table. Il peut s'agir d'une requête stockée (vue ou procédure), par exemple.</span><span class="sxs-lookup"><span data-stu-id="a53f2-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a53f2-119"><em>conteneur</em></span><span class="sxs-lookup"><span data-stu-id="a53f2-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="a53f2-120">Nom d'un conteneur valide.</span><span class="sxs-lookup"><span data-stu-id="a53f2-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a53f2-121"><em>nomautorisation</em></span><span class="sxs-lookup"><span data-stu-id="a53f2-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="a53f2-122">Nom d'utilisateur ou de groupe.</span><span class="sxs-lookup"><span data-stu-id="a53f2-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

