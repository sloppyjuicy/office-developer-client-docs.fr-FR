---
title: Connection Members (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 001cb1372acf4a4a55b3841a3f4ca8d6598f55e8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469863"
---
# <a name="connection-members-dao"></a><span data-ttu-id="b7e55-102">Connection Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="b7e55-102">Connection Members (DAO)</span></span>


<span data-ttu-id="b7e55-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7e55-103">**Applies to**: Access 2013 | Office 2013</span></span>


> [!NOTE]
> <P><span data-ttu-id="b7e55-104">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="b7e55-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="b7e55-105">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.Un objet Connection représente une connexion à une base de données ODBC (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="b7e55-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.A Connection object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span></P>



## <a name="methods"></a><span data-ttu-id="b7e55-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b7e55-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7e55-107">Nom</span><span class="sxs-lookup"><span data-stu-id="b7e55-107">Name</span></span></p></th>
<th><p><span data-ttu-id="b7e55-108">Description</span><span class="sxs-lookup"><span data-stu-id="b7e55-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7e55-109"><strong><a href="connection-cancel-method-dao.md">Annuler</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-109"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="b7e55-p102">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b7e55-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="b7e55-112">Annule l'exécution d'un appel asynchrone de méthode en attente (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="b7e55-112">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e55-113"><strong><a href="connection-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-113"><strong><a href="connection-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-114">Ferme un objet <strong>Connection</strong> ouvert.</span><span class="sxs-lookup"><span data-stu-id="b7e55-114">Closes an open <strong>Connection</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e55-115"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-115"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-116">Crée un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="b7e55-116">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e55-117"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-117"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-118">Exécute une requête Action ou une instruction SQL sur l'objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7e55-118">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e55-119"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-119"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-120">Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> et l'ajoute à la collection <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7e55-120">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="b7e55-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7e55-121">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7e55-122">Nom</span><span class="sxs-lookup"><span data-stu-id="b7e55-122">Name</span></span></p></th>
<th><p><span data-ttu-id="b7e55-123">Description</span><span class="sxs-lookup"><span data-stu-id="b7e55-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7e55-124"><strong><a href="connection-connect-property-dao.md">Se connecter</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-124"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-p103">Définit ou renvoie une valeur qui fournit des informations sur la source d'une connexion ouverte. Valeur de type <strong>String</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b7e55-p103">Sets or returns a value that provides information about the source of an open connection. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e55-127"><strong><a href="connection-database-property-dao.md">Base de données</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-127"><strong><a href="connection-database-property-dao.md">Database</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="b7e55-p104">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b7e55-p104">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="b7e55-130">Renvoie l'objet <strong><a href="database-object-dao.md">Database</a></strong> qui correspond à cette connexion (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="b7e55-130">Returns the <strong><a href="database-object-dao.md">Database</a></strong> object that corresponds to this connection (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e55-131"><strong><a href="connection-name-property-dao.md">Nom</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-131"><strong><a href="connection-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-132">Renvoie le nom d'un objet <strong><a href="connection-object-dao.md">Connection</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="b7e55-132">Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e55-133"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-133"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-p105">Renvoie une collection <strong>QueryDefs</strong> qui contient tous les objets <strong>QueryDef</strong> de la connexion spécifiée. Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b7e55-p105">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified connection. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e55-136"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-136"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-137">Définit ou retourne une valeur qui spécifie le nombre de secondes d'attente avant qu'une erreur de délai d'attente soit générée lors de l'exécution d'une requête sur une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="b7e55-137">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e55-138"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-138"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-139">Renvoie le nombre d'enregistrements affectés par le dernier appel de la méthode <strong><a href="connection-execute-method-dao.md">Execute</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="b7e55-139">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e55-140"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-140"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-p106">Renvoie une collection <strong>Recordsets</strong> qui contient tous les jeux d'enregistrements ouverts pour la connexion spécifiée. Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b7e55-p106">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified connection. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e55-143"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-143"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="b7e55-p107">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b7e55-p107">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="b7e55-146">Indique si l'exécution d'une opération asynchrone (c.-à-d. une méthode appelée avec l'option <strong>dbRunAsync</strong>) est terminée (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="b7e55-146">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7e55-147"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-147"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-p108">Renvoie une valeur qui indique si un objet prend en charge les transactions. Valeur <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b7e55-p108">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7e55-150"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="b7e55-150"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b7e55-p109">Renvoie une valeur qui indique si vous pouvez changer un objet DAO. Type de données <strong>Boolean</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b7e55-p109">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

