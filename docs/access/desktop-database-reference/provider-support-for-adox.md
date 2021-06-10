---
title: Prise en charge du fournisseur pour ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a92ffe9b4b713518330d9dbfd9979d904a5abe8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301098"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="f6584-102">Prise en charge du fournisseur pour ADOX</span><span class="sxs-lookup"><span data-stu-id="f6584-102">Provider support for ADOX</span></span>


<span data-ttu-id="f6584-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6584-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6584-p101">Selon votre fournisseur de données OLE DB, certaines fonctionnalités d'ADOX ne sont pas prises en charge. ADOX est complètement pris en charge par le [fournisseur Microsoft OLE DB pour Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Les fonctionnalités non prises en charge par le [fournisseur Microsoft OLE DB pour SQL Server](microsoft-ole-db-provider-for-sql-server.md), le [fournisseur Microsoft OLE DB pour ODBC](microsoft-ole-db-provider-for-odbc.md) ou le [fournisseur Microsoft OLE DB pour Oracle](microsoft-ole-db-provider-for-oracle.md) sont répertoriées ci-dessous. ADOX n'est pas pris en charge par d'autres fournisseurs Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f6584-p101">Certain features of ADOX are unsupported, depending upon your OLE DB data provider. ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below. ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="f6584-108">Fournisseur Microsoft OLE DB pour SQL Server</span><span class="sxs-lookup"><span data-stu-id="f6584-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6584-109">Objet ou collection</span><span class="sxs-lookup"><span data-stu-id="f6584-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="f6584-110">Restriction d'utilisation</span><span class="sxs-lookup"><span data-stu-id="f6584-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6584-111">Objet <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f6584-112">La méthode <strong>Create</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-113">Collection <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-114">Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</span><span class="sxs-lookup"><span data-stu-id="f6584-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6584-115">Collection <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-116">La collection <strong>Views</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-117">Collection <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-118">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6584-119">Objet <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f6584-120">La propriété <strong>Command</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-121">Collection <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-122">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6584-123">Collection <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-124">La collection <strong>Users</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-125">Collection <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-126">La collection <strong>Groups</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="f6584-127">Fournisseur Microsoft OLE DB pour ODBC</span><span class="sxs-lookup"><span data-stu-id="f6584-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6584-128">Objet ou collection</span><span class="sxs-lookup"><span data-stu-id="f6584-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="f6584-129">Restriction d'utilisation</span><span class="sxs-lookup"><span data-stu-id="f6584-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6584-130">Objet <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f6584-131">La méthode <strong>Create</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-132">Collection <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-133">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="f6584-134">Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</span><span class="sxs-lookup"><span data-stu-id="f6584-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6584-135">Collection <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-136">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-137">Objet <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f6584-138">La propriété <strong>Command</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6584-139">Collection  <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-140">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-141">Collection <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-142">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6584-143">Collection <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-144">La collection <strong>Users</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-145">Collection <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-146">La collection <strong>Groups</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="f6584-147">Fournisseur Microsoft OLE DB pour Oracle</span><span class="sxs-lookup"><span data-stu-id="f6584-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6584-148">Objet ou collection</span><span class="sxs-lookup"><span data-stu-id="f6584-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="f6584-149">Restriction d'utilisation</span><span class="sxs-lookup"><span data-stu-id="f6584-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6584-150">Objet <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f6584-151">La méthode <strong>Create</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-152">Collection <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-153">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="f6584-154">Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</span><span class="sxs-lookup"><span data-stu-id="f6584-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6584-155">Collection <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-156">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-157">Objet <strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f6584-158">La propriété <strong>Command</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6584-159">Collection <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f6584-160">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-161">Objet <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="f6584-162">La propriété <strong>Command</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6584-163">Collection  <strong>Indexes</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-164">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-165">Collection <strong>Keys</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-166">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6584-167">Collection <strong>Users</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-168">La collection <strong>Users</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6584-169">Collection <strong>Groups</strong></span><span class="sxs-lookup"><span data-stu-id="f6584-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="f6584-170">La collection <strong>Groups</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f6584-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

