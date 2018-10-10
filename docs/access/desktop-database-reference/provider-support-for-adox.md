---
title: Prise en charge d'ADOX par les fournisseurs
TOCTitle: Provider Support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d55ae14d124bfad7f8abbfcf3d94398ea92d792
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472249"
---
# <a name="provider-support-for-adox"></a><span data-ttu-id="ca285-102">Prise en charge d'ADOX par les fournisseurs</span><span class="sxs-lookup"><span data-stu-id="ca285-102">Provider Support for ADOX</span></span>


<span data-ttu-id="ca285-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca285-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ca285-p101">Selon votre fournisseur de données OLE DB, certaines fonctionnalités d'ADOX ne sont pas prises en charge. ADOX est complètement pris en charge par le [fournisseur Microsoft OLE DB pour Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Les fonctionnalités non prises en charge par le [fournisseur Microsoft OLE DB pour SQL Server](microsoft-ole-db-provider-for-sql-server.md), le [fournisseur Microsoft OLE DB pour ODBC](microsoft-ole-db-provider-for-odbc.md) ou le [fournisseur Microsoft OLE DB pour Oracle](microsoft-ole-db-provider-for-oracle.md) sont répertoriées ci-dessous. ADOX n'est pas pris en charge par d'autres fournisseurs Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="ca285-p101">Certain features of ADOX are unsupported, depending upon your OLE DB data provider. ADOX is fully supported with the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). The unsupported features with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), the [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md), or the [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) are listed below. ADOX is not supported by any other Microsoft OLE DB providers.</span></span>

## <a name="microsoft-ole-db-provider-for-sql-server"></a><span data-ttu-id="ca285-108">Fournisseur Microsoft OLE DB pour SQL Server</span><span class="sxs-lookup"><span data-stu-id="ca285-108">Microsoft OLE DB Provider for SQL Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca285-109">Objet ou collection</span><span class="sxs-lookup"><span data-stu-id="ca285-109">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="ca285-110">Restriction d'utilisation</span><span class="sxs-lookup"><span data-stu-id="ca285-110">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca285-111">Objet <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-111"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ca285-112">La méthode <strong>Create</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-112">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-113">Collection <strong>Tables</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-113"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-114">Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</span><span class="sxs-lookup"><span data-stu-id="ca285-114">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca285-115">Collection <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-115"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-116">La collection <strong>Views</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-116"><strong>Views</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-117"><strong>Procedures</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-117"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-118">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-118">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca285-119">Objet <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-119"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ca285-120">La propriété <strong>Command</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-120">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-121"><strong>Keys</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-121"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-122">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-122">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca285-123"><strong>Users</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-123"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-124">La collection <strong>Users</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-124"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-125"><strong>Groups</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-125"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-126">La collection <strong>Groups</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-126"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a><span data-ttu-id="ca285-127">Fournisseur Microsoft OLE DB pour ODBC</span><span class="sxs-lookup"><span data-stu-id="ca285-127">Microsoft OLE DB Provider for ODBC</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca285-128">Objet ou collection</span><span class="sxs-lookup"><span data-stu-id="ca285-128">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="ca285-129">Restriction d'utilisation</span><span class="sxs-lookup"><span data-stu-id="ca285-129">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca285-130">Objet <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-130"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ca285-131">La méthode <strong>Create</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-131">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-132"><strong>Tables</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-132"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-133">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.
</span><span class="sxs-lookup"><span data-stu-id="ca285-133">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="ca285-134">Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</span><span class="sxs-lookup"><span data-stu-id="ca285-134">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca285-135">Collection <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-135"><strong>Procedures</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-136">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-136">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-137">Objet <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-137"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ca285-138">La propriété <strong>Command</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-138">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca285-139"><strong>Indexes</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-139"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-140">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-140">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-141"><strong>Keys</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-141"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-142">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-142">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca285-143"><strong>Users</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-143"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-144">La collection <strong>Users</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-144"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-145"><strong>Groups</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-145"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-146">La collection <strong>Groups</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-146"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="ca285-147">Fournisseur Microsoft OLE DB pour Oracle</span><span class="sxs-lookup"><span data-stu-id="ca285-147">Microsoft OLE DB Provider for Oracle</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca285-148">Objet ou collection</span><span class="sxs-lookup"><span data-stu-id="ca285-148">Object or Collection</span></span></p></th>
<th><p><span data-ttu-id="ca285-149">Restriction d'utilisation</span><span class="sxs-lookup"><span data-stu-id="ca285-149">Usage Restriction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca285-150">Objet <strong>Catalog</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-150"><strong>Catalog</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ca285-151">La méthode <strong>Create</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-151">The <strong>Create</strong> method is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-152"><strong>Tables</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-152"><strong>Tables</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-153">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.
</span><span class="sxs-lookup"><span data-stu-id="ca285-153">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span> <span data-ttu-id="ca285-154">Les propriétés sont en lecture/écriture avant la création de l'objet et en lecture seule en cas de référence à un objet existant.</span><span class="sxs-lookup"><span data-stu-id="ca285-154">Properties are read/write prior to object creation, and read-only when referencing an existing object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca285-155">Collection <strong>Views</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-155"><strong>Views</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-156">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-156">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-157">Objet <strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-157"><strong>View</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ca285-158">La propriété <strong>Command</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-158">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca285-159">Collection <strong>Procedures</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-159"><strong>Procedures</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ca285-160">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-160">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-161">Objet <strong>Procedure</strong></span><span class="sxs-lookup"><span data-stu-id="ca285-161"><strong>Procedure</strong> object</span></span></p></td>
<td><p><span data-ttu-id="ca285-162">La propriété <strong>Command</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-162">The <strong>Command</strong> property is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca285-163"><strong>Indexes</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-163"><strong>Indexes</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-164">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-164">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-165"><strong>Keys</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-165"><strong>Keys</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-166">Les méthodes <strong>Append</strong> et <strong>Delete</strong> ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-166">The <strong>Append</strong> and <strong>Delete</strong> methods are not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca285-167"><strong>Users</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-167"><strong>Users</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-168">La collection <strong>Users</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-168"><strong>Users</strong> is not supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca285-169"><strong>Groups</strong> , collection</span><span class="sxs-lookup"><span data-stu-id="ca285-169"><strong>Groups</strong> collection</span></span></p></td>
<td><p><span data-ttu-id="ca285-170">La collection <strong>Groups</strong> n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ca285-170"><strong>Groups</strong> is not supported.</span></span></p></td>
</tr>
</tbody>
</table>

