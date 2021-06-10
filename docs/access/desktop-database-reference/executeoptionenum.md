---
title: ExecuteOptionEnum (référence de base de données de bureau Access)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: febeb3b52eb579647c995b01d6723a5c1f1b0c1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293244"
---
# <a name="executeoptionenum"></a><span data-ttu-id="27777-102">ExecuteOptionEnum</span><span class="sxs-lookup"><span data-stu-id="27777-102">ExecuteOptionEnum</span></span>

<span data-ttu-id="27777-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27777-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27777-104">Spécifie la manière dont un fournisseur doit exécuter une commande.</span><span class="sxs-lookup"><span data-stu-id="27777-104">Specifies how a provider should execute a command.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27777-105">Constante</span><span class="sxs-lookup"><span data-stu-id="27777-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="27777-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="27777-106">Value</span></span></p></th>
<th><p><span data-ttu-id="27777-107">Description</span><span class="sxs-lookup"><span data-stu-id="27777-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27777-108"><strong>adAsyncExecute</strong></span><span class="sxs-lookup"><span data-stu-id="27777-108"><strong>adAsyncExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="27777-109">0x10</span><span class="sxs-lookup"><span data-stu-id="27777-109">0x10</span></span></p></td>
<td><p><span data-ttu-id="27777-110">Indique que la commande doit s’exécuter de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="27777-110">Indicates that the command should execute asynchronously.</span></span> <span data-ttu-id="27777-111">Cette valeur ne peut être combinée avec la valeur <a href="commandtypeenum.md">CommandTypeEnum</a><strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="27777-111">This value cannot be combined with the <a href="commandtypeenum.md">CommandTypeEnum</a> value <strong>adCmdTableDirect</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27777-112"><strong>adAsyncFetch</strong></span><span class="sxs-lookup"><span data-stu-id="27777-112"><strong>adAsyncFetch</strong></span></span></p></td>
<td><p><span data-ttu-id="27777-113">0x20</span><span class="sxs-lookup"><span data-stu-id="27777-113">0x20</span></span></p></td>
<td><p><span data-ttu-id="27777-114">Indique que les lignes restantes après la quantité spécifiée dans la propriété <a href="cachesize-property-ado.md">CacheSize</a> doivent être extraites de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="27777-114">Indicates that the remaining rows after the initial quantity specified in the <a href="cachesize-property-ado.md">CacheSize</a> property should be retrieved asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27777-115"><strong>adAsyncFetchNonBlocking</strong></span><span class="sxs-lookup"><span data-stu-id="27777-115"><strong>adAsyncFetchNonBlocking</strong></span></span></p></td>
<td><p><span data-ttu-id="27777-116">0x40</span><span class="sxs-lookup"><span data-stu-id="27777-116">0x40</span></span></p></td>
<td><p><span data-ttu-id="27777-p102">Indique que le thème principal ne bloque jamais l'extraction. Si la ligne demandée n'a pas été extraite, la ligne en cours se déplace automatiquement vers la fin du fichier.
</span><span class="sxs-lookup"><span data-stu-id="27777-p102">Indicates that the main thread never blocks while retrieving. If the requested row has not been retrieved, the current row automatically moves to the end of the file.</span></span></p><p><span data-ttu-id="27777-119">Si vous ouvrez un objet <a href="recordset-object-ado.md">Recordset</a> depuis une <a href="stream-object-ado.md">chaîne</a> contenant un objet <strong>Recordset</strong> stocké avec persistance, <strong>adAsyncFetchNonBlocking</strong> sera sans effet ; l’opération sera synchrone et bloquante.</span><span class="sxs-lookup"><span data-stu-id="27777-119">If you open a <a href="recordset-object-ado.md">Recordset</a> from a <a href="stream-object-ado.md">Stream</a> containing a persistently stored <strong>Recordset</strong>, <strong>adAsyncFetchNonBlocking</strong> will not have an effect; the operation will be synchronous and blocking.</span></span> <span data-ttu-id="27777-120"><strong>adAsynchFetchNonBlocking</strong> est sans effet lorsque l’option <a href="commandtypeenum.md">adCmdTableDirect</a> est utilisée pour ouvrir l’objet <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="27777-120"><strong>adAsynchFetchNonBlocking</strong> has no effect when the <a href="commandtypeenum.md">adCmdTableDirect</a> option is used to open the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27777-121"><strong>adExecuteNoRecords</strong></span><span class="sxs-lookup"><span data-stu-id="27777-121"><strong>adExecuteNoRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="27777-122">0x80</span><span class="sxs-lookup"><span data-stu-id="27777-122">0x80</span></span></p></td>
<td><p><span data-ttu-id="27777-123">Indique que le texte de la commande est une commande ou une procédure stockée qui ne renvoie pas de lignes (par exemple, une commande qui ne fait qu'insérer des données).</span><span class="sxs-lookup"><span data-stu-id="27777-123">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</span></span> <span data-ttu-id="27777-124">Si des lignes sont extraites, elles sont ignorées et non renvoyées.</span><span class="sxs-lookup"><span data-stu-id="27777-124">If any rows are retrieved, they are discarded and not returned.</span></span> <span data-ttu-id="27777-125"><strong>adExecuteNoRecords peut</strong> uniquement être transmis en tant que paramètre facultatif à la <strong>méthode Command</strong> ou <strong>Connection</strong> <strong>Execute.</strong></span><span class="sxs-lookup"><span data-stu-id="27777-125"><strong>adExecuteNoRecords</strong> can only be passed as an optional parameter to the <strong>Command</strong> or <strong>Connection</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27777-126"><strong>adExecuteStream</strong></span><span class="sxs-lookup"><span data-stu-id="27777-126"><strong>adExecuteStream</strong></span></span></p></td>
<td><p><span data-ttu-id="27777-127">0x400</span><span class="sxs-lookup"><span data-stu-id="27777-127">0x400</span></span></p></td>
<td><p><span data-ttu-id="27777-128">Indique que le résultat de l'exécution d'une commande doit être renvoyé sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="27777-128">Indicates that the results of a command execution should be returned as a stream.</span></span> <span data-ttu-id="27777-129"><strong>adExecuteStream</strong> peut uniquement être transmis en tant que paramètre facultatif à la <strong>méthode Command</strong> <strong>Execute.</strong></span><span class="sxs-lookup"><span data-stu-id="27777-129"><strong>adExecuteStream</strong> can only be passed as an optional parameter to the <strong>Command</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27777-130"><strong>adExecuteRecord</strong></span><span class="sxs-lookup"><span data-stu-id="27777-130"><strong>adExecuteRecord</strong></span></span></p></td>
<td><p><br />
</p></td>
<td><p><span data-ttu-id="27777-131">Indique que <strong>CommandText</strong> est une commande ou une procédure stockée qui renvoie une seule ligne, sous la forme d'un objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="27777-131">Indicates that the <strong>CommandText</strong> is a command or stored procedure that returns a single row which should be returned as a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27777-132"><strong>adOptionUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="27777-132"><strong>adOptionUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="27777-133">-1</span><span class="sxs-lookup"><span data-stu-id="27777-133">-1</span></span></p></td>
<td><p><span data-ttu-id="27777-134">Indique que la commande n'est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="27777-134">Indicates that the command is unspecified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="27777-135">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="27777-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="27777-136">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="27777-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27777-137">Constante</span><span class="sxs-lookup"><span data-stu-id="27777-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27777-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span><span class="sxs-lookup"><span data-stu-id="27777-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27777-139">AdoEnums.ExecuteOption.ASYNCFETCH</span><span class="sxs-lookup"><span data-stu-id="27777-139">AdoEnums.ExecuteOption.ASYNCFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27777-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span><span class="sxs-lookup"><span data-stu-id="27777-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27777-141">AdoEnums.ExecuteOption.NORECORDS</span><span class="sxs-lookup"><span data-stu-id="27777-141">AdoEnums.ExecuteOption.NORECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27777-142">AdoEnums.ExecuteOption.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="27777-142">AdoEnums.ExecuteOption.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

