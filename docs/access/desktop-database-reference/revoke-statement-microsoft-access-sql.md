---
title: REVOKE, instruction (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306530"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="03cf0-102">REVOKE, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="03cf0-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="03cf0-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03cf0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03cf0-104">Révoque des privilèges spécifiques à un utilisateur ou à un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="03cf0-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="03cf0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03cf0-105">Syntax</span></span>

<span data-ttu-id="03cf0-106">Revoke {*privilège*\[, *privilège*,... \]} Sur {table *table* | Object, *objet*|</span><span class="sxs-lookup"><span data-stu-id="03cf0-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="03cf0-107">*Conteneur*de connomautorisation\*\*\[, *nomautorisation*,... \]}</span><span class="sxs-lookup"><span data-stu-id="03cf0-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="03cf0-108">L'instruction REVOKE est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="03cf0-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03cf0-109">Élément</span><span class="sxs-lookup"><span data-stu-id="03cf0-109">Part</span></span></p></th>
<th><p><span data-ttu-id="03cf0-110">Description</span><span class="sxs-lookup"><span data-stu-id="03cf0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03cf0-111"><em>privilège</em></span><span class="sxs-lookup"><span data-stu-id="03cf0-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="03cf0-112">Le ou les privilèges à révoquer.</span><span class="sxs-lookup"><span data-stu-id="03cf0-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="03cf0-113">Les privilèges sont spécifiés à l'aide des mots clés suivants: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATe, SELECTSCHEMA, SCHEMA et UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="03cf0-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03cf0-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="03cf0-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="03cf0-115">Tout nom de table valide.</span><span class="sxs-lookup"><span data-stu-id="03cf0-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03cf0-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="03cf0-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="03cf0-117">Tout objet autre qu'une table.</span><span class="sxs-lookup"><span data-stu-id="03cf0-117">This can encompass any non-table object.</span></span> <span data-ttu-id="03cf0-118">Il peut s'agir d'une requête stockée (vue ou procédure), par exemple.</span><span class="sxs-lookup"><span data-stu-id="03cf0-118">A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03cf0-119"><em>conteneur</em></span><span class="sxs-lookup"><span data-stu-id="03cf0-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="03cf0-120">Nom d'un conteneur valide.</span><span class="sxs-lookup"><span data-stu-id="03cf0-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03cf0-121"><em>nomautorisation</em></span><span class="sxs-lookup"><span data-stu-id="03cf0-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="03cf0-122">Nom d'utilisateur ou de groupe.</span><span class="sxs-lookup"><span data-stu-id="03cf0-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

