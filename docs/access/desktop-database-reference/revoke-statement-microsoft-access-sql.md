---
title: RÉVOQUER l’instruction (Microsoft Access SQL)
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
ms.openlocfilehash: c3a7a64eee4617c07c1a655e34223f0531e16b18
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890896"
---
# <a name="revoke-statement-microsoft-access-sql"></a><span data-ttu-id="2dc7b-102">RÉVOQUER l’instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="2dc7b-102">REVOKE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="2dc7b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2dc7b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2dc7b-104">Révoque des privilèges spécifiques à un utilisateur ou à un groupe existant.</span><span class="sxs-lookup"><span data-stu-id="2dc7b-104">Revokes specific privileges from an existing user or group.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc7b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2dc7b-105">Syntax</span></span>

<span data-ttu-id="2dc7b-106">REVOKE {*privilège*\[, *privilège*, … \]} ON {TABLE *table* | OBJET, *objet*|</span><span class="sxs-lookup"><span data-stu-id="2dc7b-106">REVOKE {*privilege*\[, *privilege*, …\]} ON {TABLE *table* | OBJECT *object*|</span></span>

<span data-ttu-id="2dc7b-107">{Container *conteneur*} FROM {*nomautorisation*\[, *nomautorisation*, … \]}</span><span class="sxs-lookup"><span data-stu-id="2dc7b-107">CONTAINTER *container*} FROM {*authorizationname*\[, *authorizationname*, …\]}</span></span>

<span data-ttu-id="2dc7b-108">L'instruction REVOKE est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2dc7b-108">The REVOKE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2dc7b-109">Argument</span><span class="sxs-lookup"><span data-stu-id="2dc7b-109">Part</span></span></p></th>
<th><p><span data-ttu-id="2dc7b-110">Description</span><span class="sxs-lookup"><span data-stu-id="2dc7b-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dc7b-111"><em>privilège</em></span><span class="sxs-lookup"><span data-stu-id="2dc7b-111"><em>privilege</em></span></span></p></td>
<td><p><span data-ttu-id="2dc7b-112">L’ou les privilèges à révoquer.</span><span class="sxs-lookup"><span data-stu-id="2dc7b-112">The privilege or privileges to be revoked.</span></span> <span data-ttu-id="2dc7b-113">Les privilèges sont spécifiés à l’aide de mots clés suivants : sélectionnez, DELETE, INSERT, UPDATE, dépôt, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA et UPDATEOWNER.</span><span class="sxs-lookup"><span data-stu-id="2dc7b-113">Privileges are specified using the following keywords: SELECT, DELETE, INSERT, UPDATE, DROP, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, CREATE, SELECTSCHEMA, SCHEMA, and UPDATEOWNER.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dc7b-114"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="2dc7b-114"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="2dc7b-115">Tout nom de table valide.</span><span class="sxs-lookup"><span data-stu-id="2dc7b-115">Any valid table name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dc7b-116"><em>object</em></span><span class="sxs-lookup"><span data-stu-id="2dc7b-116"><em>object</em></span></span></p></td>
<td><p><span data-ttu-id="2dc7b-p102">Tout objet autre qu'une table. Il peut s'agir d'une requête stockée (vue ou procédure), par exemple.</span><span class="sxs-lookup"><span data-stu-id="2dc7b-p102">This can encompass any non-table object. A stored query (view or procedure) is one example.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dc7b-119"><em>conteneur</em></span><span class="sxs-lookup"><span data-stu-id="2dc7b-119"><em>container</em></span></span></p></td>
<td><p><span data-ttu-id="2dc7b-120">Nom d'un conteneur valide.</span><span class="sxs-lookup"><span data-stu-id="2dc7b-120">The name of a valid container.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dc7b-121"><em>nomautorisation</em></span><span class="sxs-lookup"><span data-stu-id="2dc7b-121"><em>authorizationname</em></span></span></p></td>
<td><p><span data-ttu-id="2dc7b-122">Nom d'utilisateur ou de groupe.</span><span class="sxs-lookup"><span data-stu-id="2dc7b-122">A user or group name.</span></span></p></td>
</tr>
</tbody>
</table>

