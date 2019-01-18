---
title: Méthode Connection.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b6600d4508a33a31098d6a2e7c92f5904beb0e95
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705931"
---
# <a name="connectioncreatequerydef-method-dao"></a><span data-ttu-id="e9ade-102">Méthode Connection.CreateQueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="e9ade-102">Connection.CreateQueryDef method (DAO)</span></span>

<span data-ttu-id="e9ade-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9ade-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9ade-104">Crée un objet **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e9ade-104">Creates a new **[QueryDef](querydef-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ade-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9ade-105">Syntax</span></span>

<span data-ttu-id="e9ade-106">*expression* . CreateQueryDef (***nom***, ***SQLText***)</span><span class="sxs-lookup"><span data-stu-id="e9ade-106">*expression* .CreateQueryDef(***Name***, ***SQLText***)</span></span>

<span data-ttu-id="e9ade-107">*expression* Variable qui représente un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="e9ade-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9ade-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9ade-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9ade-109">Nom</span><span class="sxs-lookup"><span data-stu-id="e9ade-109">Name</span></span></p></th>
<th><p><span data-ttu-id="e9ade-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="e9ade-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="e9ade-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="e9ade-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="e9ade-112">Description</span><span class="sxs-lookup"><span data-stu-id="e9ade-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9ade-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="e9ade-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="e9ade-114">Facultatif</span><span class="sxs-lookup"><span data-stu-id="e9ade-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="e9ade-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e9ade-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e9ade-116"><strong>Variant</strong> (sous-type <strong>String</strong>) qui identifie par un nom unique le nouvel objet <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9ade-116">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9ade-117"><em>SQLText</em></span><span class="sxs-lookup"><span data-stu-id="e9ade-117"><em>SQLText</em></span></span></p></td>
<td><p><span data-ttu-id="e9ade-118">Facultatif</span><span class="sxs-lookup"><span data-stu-id="e9ade-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="e9ade-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e9ade-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e9ade-p101"><strong>Variant</strong> (sous-type <strong>String</strong>) qui représente une instruction SQL définissant l’objet <strong>QueryDef</strong>. Si vous ne spécifiez pas cet argument, vous pouvez définir l’objet <strong>QueryDef</strong> en paramétrant sa propriété <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> avant ou après son ajout à une collection.</span><span class="sxs-lookup"><span data-stu-id="e9ade-p101">A <strong>Variant</strong> (<strong>String</strong> subtype) that is an SQL statement defining the <strong>QueryDef</strong>. If you omit this argument, you can define the <strong>QueryDef</strong> by setting its <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> property before or after you append it to a collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="e9ade-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e9ade-122">Return value</span></span>

<span data-ttu-id="e9ade-123">QueryDef</span><span class="sxs-lookup"><span data-stu-id="e9ade-123">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="e9ade-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="e9ade-124">Remarks</span></span>

<span data-ttu-id="e9ade-125">Dans un espace de travail Microsoft Access, si vous spécifiez autre chose qu'une chaîne de longueur nulle pour le nom lorsque vous créez un objet **QueryDef**, l'objet **QueryDef** résultant est automatiquement ajouté à la collection **[QueryDefs](querydefs-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e9ade-125">In a Microsoft Access workspace, if you provide anything other than a zero-length string for the name when you create a **QueryDef**, the resulting **QueryDef** object is automatically appended to the **[QueryDefs](querydefs-collection-dao.md)** collection.</span></span>

<span data-ttu-id="e9ade-126">Si l’objet spécifié par un nom est déjà membre de la collection **QueryDefs** , une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="e9ade-126">If the object specified by name is already a member of the **QueryDefs** collection, a run-time error occurs.</span></span> <span data-ttu-id="e9ade-127">Vous pouvez créer un **objet QueryDef** temporaire à l’aide d’une chaîne de longueur nulle pour l’argument nom lorsque vous exécutez la méthode **CreateQueryDef** .</span><span class="sxs-lookup"><span data-stu-id="e9ade-127">You can create a temporary **QueryDef** by using a zero-length string for the name argument when you execute the **CreateQueryDef** method.</span></span> <span data-ttu-id="e9ade-128">Vous obtenez un résultat identique en affectant à la propriété **[Name](connection-name-property-dao.md)** d'un nouvel objet **QueryDef** une chaîne nulle ("").</span><span class="sxs-lookup"><span data-stu-id="e9ade-128">You can also accomplish this by setting the **[Name](connection-name-property-dao.md)** property of a newly created **QueryDef** to a zero-length string ("").</span></span> <span data-ttu-id="e9ade-129">Les objets **QueryDef** temporaires sont utiles si vous souhaitez utiliser à plusieurs reprises des instructions SQL dynamiques sans créer de nouveaux objets permanents dans la collection **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="e9ade-129">Temporary **QueryDef** objects are useful if you want to repeatedly use dynamic SQL statements without having to create any new permanent objects in the **QueryDefs** collection.</span></span> <span data-ttu-id="e9ade-130">Vous ne pouvez pas ajouter d'objet **QueryDef** temporaire à une collection car une chaîne nulle ne constitue pas un nom valide pour un objet **QueryDef** permanent.</span><span class="sxs-lookup"><span data-stu-id="e9ade-130">You can't append a temporary **QueryDef** to any collection because a zero-length string isn't a valid name for a permanent **QueryDef** object.</span></span> <span data-ttu-id="e9ade-131">Vous avez toujours la possibilité de définir les propriétés **Name** et **SQL** du nouvel objet **QueryDef** et ajouter par la suite l'objet **QueryDef** à la collection **QueryDefs**.</span><span class="sxs-lookup"><span data-stu-id="e9ade-131">You can always set the **Name** and **SQL** properties of the newly created **QueryDef** object and subsequently append the **QueryDef** to the **QueryDefs** collection.</span></span>

<span data-ttu-id="e9ade-132">Pour exécuter l'instruction SQL dans un objet **QueryDef**, utilisez la méthode **[Execute](connection-execute-method-dao.md)** ou **[OpenRecordset](connection-openrecordset-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e9ade-132">To run the SQL statement in a **QueryDef** object, use the **[Execute](connection-execute-method-dao.md)** or **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span>

<span data-ttu-id="e9ade-133">Le recours à un objet **QueryDef** est la méthode généralement utilisée pour exécuter des requêtes SQL directes avec des bases de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="e9ade-133">Using a **QueryDef** object is the preferred way to perform SQL pass-through queries with ODBC databases.</span></span>

<span data-ttu-id="e9ade-134">Pour supprimer un objet **QueryDef** d'une collection **QueryDefs** dans une base de données de moteur de base de données Microsoft Access, appelez la méthode **[Delete](fields-delete-method-dao.md)** sur la collection.</span><span class="sxs-lookup"><span data-stu-id="e9ade-134">To remove a **QueryDef** object from a **QueryDefs** collection in a Microsoft Access database engine database, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

