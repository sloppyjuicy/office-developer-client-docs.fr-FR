---
title: CommandTypeEnum (référence de base de données du bureau Access)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9114128771d4753265208dada763ac0c9f796d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714275"
---
# <a name="commandtypeenum"></a><span data-ttu-id="aaec0-102">CommandTypeEnum</span><span class="sxs-lookup"><span data-stu-id="aaec0-102">CommandTypeEnum</span></span>

<span data-ttu-id="aaec0-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aaec0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aaec0-104">Spécifie comment interpréter un argument de commande.</span><span class="sxs-lookup"><span data-stu-id="aaec0-104">Specifies how a command argument should be interpreted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aaec0-105">Constante</span><span class="sxs-lookup"><span data-stu-id="aaec0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="aaec0-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaec0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="aaec0-107">Description</span><span class="sxs-lookup"><span data-stu-id="aaec0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aaec0-108"><strong>adCmdUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="aaec0-108"><strong>adCmdUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="aaec0-109">-1</span><span class="sxs-lookup"><span data-stu-id="aaec0-109">-1</span></span></p></td>
<td><p><span data-ttu-id="aaec0-110">Ne spécifie pas l'argument du type de commande.</span><span class="sxs-lookup"><span data-stu-id="aaec0-110">Does not specify the command type argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaec0-111"><strong>adCmdText</strong></span><span class="sxs-lookup"><span data-stu-id="aaec0-111"><strong>adCmdText</strong></span></span></p></td>
<td><p><span data-ttu-id="aaec0-112">1</span><span class="sxs-lookup"><span data-stu-id="aaec0-112">1</span></span></p></td>
<td><p><span data-ttu-id="aaec0-113">Evalue <a href="commandtext-property-ado.md">CommandText</a> comme définition textuelle d’une commande ou d’un appel de procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="aaec0-113">Evaluates <a href="commandtext-property-ado.md">CommandText</a> as a textual definition of a command or stored procedure call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaec0-114"><strong>valeur Command.CommandType</strong></span><span class="sxs-lookup"><span data-stu-id="aaec0-114"><strong>adCmdTable</strong></span></span></p></td>
<td><p><span data-ttu-id="aaec0-115">2</span><span class="sxs-lookup"><span data-stu-id="aaec0-115">2</span></span></p></td>
<td><p><span data-ttu-id="aaec0-116">Evalue <strong>CommandText</strong> comme nom de table dont les colonnes sont toutes renvoyées par une requête SQL générée en interne.</span><span class="sxs-lookup"><span data-stu-id="aaec0-116">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned by an internally generated SQL query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaec0-117"><strong>valeur adCmdStoredProc</strong></span><span class="sxs-lookup"><span data-stu-id="aaec0-117"><strong>adCmdStoredProc</strong></span></span></p></td>
<td><p><span data-ttu-id="aaec0-118">4</span><span class="sxs-lookup"><span data-stu-id="aaec0-118">4</span></span></p></td>
<td><p><span data-ttu-id="aaec0-119">Evalue <strong>CommandText</strong> comme nom de procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="aaec0-119">Evaluates <strong>CommandText</strong> as a stored procedure name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaec0-120"><strong>adCmdUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="aaec0-120"><strong>adCmdUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="aaec0-121">8</span><span class="sxs-lookup"><span data-stu-id="aaec0-121">8</span></span></p></td>
<td><p><span data-ttu-id="aaec0-p101">Par défaut. Indique que le type de la commande dans la propriété <strong>CommandText</strong> n'est pas connu.</span><span class="sxs-lookup"><span data-stu-id="aaec0-p101">Default. Indicates that the type of command in the <strong>CommandText</strong> property is not known.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaec0-124"><strong>adCmdFile</strong></span><span class="sxs-lookup"><span data-stu-id="aaec0-124"><strong>adCmdFile</strong></span></span></p></td>
<td><p><span data-ttu-id="aaec0-125">256</span><span class="sxs-lookup"><span data-stu-id="aaec0-125">256</span></span></p></td>
<td><p><span data-ttu-id="aaec0-p102">Evalue <strong>CommandText</strong> comme nom de fichier d’un <a href="recordset-object-ado.md">Recordset</a> stocké avec persistance. S’utilise uniquement avec <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> et <a href="requery-method-ado.md">Requery</a>.</span><span class="sxs-lookup"><span data-stu-id="aaec0-p102">Evaluates <strong>CommandText</strong> as the file name of a persistently stored <a href="recordset-object-ado.md">Recordset</a>. Used with <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> or <a href="requery-method-ado.md">Requery</a> only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaec0-128"><strong>adCmdTableDirect</strong></span><span class="sxs-lookup"><span data-stu-id="aaec0-128"><strong>adCmdTableDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="aaec0-129">512</span><span class="sxs-lookup"><span data-stu-id="aaec0-129">512</span></span></p></td>
<td><p><span data-ttu-id="aaec0-130">Evalue <strong>CommandText</strong> comme nom de table dont les colonnes sont toutes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="aaec0-130">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned.</span></span> <span data-ttu-id="aaec0-131">Utilisé uniquement avec <strong>Recordset.Open</strong> et <strong>Requery</strong> .</span><span class="sxs-lookup"><span data-stu-id="aaec0-131">Used with <strong>Recordset.Open</strong> or <strong>Requery</strong> only.</span></span> <span data-ttu-id="aaec0-132">Pour utiliser la méthode <a href="seek-method-ado.md">Seek</a> , le <strong>Recordset</strong> doit être ouvert avec <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="aaec0-132">To use the <a href="seek-method-ado.md">Seek</a> method, the <strong>Recordset</strong> must be opened with <strong>adCmdTableDirect</strong>.</span></span> <span data-ttu-id="aaec0-133">Cette valeur ne peut être combinée avec la valeur <a href="executeoptionenum.md">ExecuteOptionEnum </a><strong>adAsyncExecute</strong>.</span><span class="sxs-lookup"><span data-stu-id="aaec0-133">This value cannot be combined with the <a href="executeoptionenum.md">ExecuteOptionEnum</a> value <strong>adAsyncExecute</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="aaec0-134">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="aaec0-134">ADO/WFC equivalent</span></span>

<span data-ttu-id="aaec0-135">Module : **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="aaec0-135">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aaec0-136">Constante</span><span class="sxs-lookup"><span data-stu-id="aaec0-136">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aaec0-137">AdoEnums.CommandType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="aaec0-137">AdoEnums.CommandType.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaec0-138">AdoEnums.CommandType.TEXT</span><span class="sxs-lookup"><span data-stu-id="aaec0-138">AdoEnums.CommandType.TEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaec0-139">AdoEnums.CommandType.TABLE</span><span class="sxs-lookup"><span data-stu-id="aaec0-139">AdoEnums.CommandType.TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaec0-140">AdoEnums.CommandType.STOREDPROC</span><span class="sxs-lookup"><span data-stu-id="aaec0-140">AdoEnums.CommandType.STOREDPROC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaec0-141">AdoEnums.CommandType.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="aaec0-141">AdoEnums.CommandType.UNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaec0-142">AdoEnums.CommandType.FILE</span><span class="sxs-lookup"><span data-stu-id="aaec0-142">AdoEnums.CommandType.FILE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaec0-143">AdoEnums.CommandType.TABLEDIRECT</span><span class="sxs-lookup"><span data-stu-id="aaec0-143">AdoEnums.CommandType.TABLEDIRECT</span></span></p></td>
</tr>
</tbody>
</table>

