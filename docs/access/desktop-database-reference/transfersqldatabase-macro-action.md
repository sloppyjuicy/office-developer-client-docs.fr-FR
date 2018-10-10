---
title: TransférerBaseDeDonnéesSQL, action de macro
TOCTitle: TransferSQLDatabase Macro Action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 301fce8bcdeff45135c305054da72f4c75f503eb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469686"
---
# <a name="transfersqldatabase-macro-action"></a><span data-ttu-id="d06ac-102">TransférerBaseDeDonnéesSQL, action de macro</span><span class="sxs-lookup"><span data-stu-id="d06ac-102">TransferSQLDatabase Macro Action</span></span>


<span data-ttu-id="d06ac-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d06ac-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d06ac-p101">Dans un projet Access, l'action **TransférerBaseDeDonnéesSQL** permet de transférer une base de données Microsoft SQL Server 7.0 ou version ultérieure vers une autre base de données SQL Server 7.0 ou version ultérieure. Pour plus d'informations sur le transfert de base de données, voir la documentation de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d06ac-p101">In an Access project, you can use the **TransferSQLDatabase** action to transfer a Microsoft SQL Server 7.0 or later database to another SQL Server 7.0 or later database. For more information on transferring a database, see the SQL Server documentation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d06ac-p102">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="d06ac-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="d06ac-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d06ac-108">Setting</span></span>

<span data-ttu-id="d06ac-109">L'action **TransférerBaseDeDonnéesSQL** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d06ac-109">The **TransferSQLDatabase** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d06ac-110">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="d06ac-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d06ac-111">Description</span><span class="sxs-lookup"><span data-stu-id="d06ac-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d06ac-112"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="d06ac-112"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ac-113">Nom du serveur de base de données SQL Server 7.0, ou version ultérieure, vers lequel la copie est effectuée.</span><span class="sxs-lookup"><span data-stu-id="d06ac-113">The name of the SQL Server 7.0 or later database server you are copying to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06ac-114"><strong>Database</strong></span><span class="sxs-lookup"><span data-stu-id="d06ac-114"><strong>Database</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ac-115">Nom de la nouvelle base de données créée sur le serveur de destination.</span><span class="sxs-lookup"><span data-stu-id="d06ac-115">The name of the new database that will be created on the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d06ac-116"><strong>Utiliser une connexion approuvée</strong></span><span class="sxs-lookup"><span data-stu-id="d06ac-116"><strong>Use Trusted Connection</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ac-117">Spécifie si ou pas il est une connexion approuvée à SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d06ac-117">Specifes whether or not there is a trusted connection to the SQL Server.</span></span> <span data-ttu-id="d06ac-118">Si la valeur <strong>Oui</strong>, il existe une connexion approuvée et les arguments <strong>connexion</strong> et <strong>mot de passe</strong> ne sont pas requis.</span><span class="sxs-lookup"><span data-stu-id="d06ac-118">If set to <strong>Yes</strong>, then there is a trusted connection and the <strong>Login</strong> and <strong>Password</strong> arguments are not required.</span></span> <span data-ttu-id="d06ac-119">Si défini sur <strong>No</strong>, le <strong>nom de connexion</strong> et <strong>le mot de passe</strong> des arguments est requis.</span><span class="sxs-lookup"><span data-stu-id="d06ac-119">If set to <strong>No</strong>, the <strong>Login</strong> and <strong>Password</strong> arguments are required.</span></span> <span data-ttu-id="d06ac-120">La valeur par défaut est <strong>Oui</strong>.</span><span class="sxs-lookup"><span data-stu-id="d06ac-120">The default is <strong>Yes</strong>.</span></span> <span data-ttu-id="d06ac-121">Lorsque vous utilisez une connexion approuvée, la sécurité de SQL Server s’intègre à la sécurité du système d’exploitation Windows pour fournir une seule sur le réseau et la base de données.</span><span class="sxs-lookup"><span data-stu-id="d06ac-121">When you use a trusted connection, SQL Server security integrates with the Windows operating system security to provide a single log on to the network and the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06ac-122"><strong>Connexion</strong></span><span class="sxs-lookup"><span data-stu-id="d06ac-122"><strong>Login</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ac-123">Identificateur de connexion au serveur de destination.</span><span class="sxs-lookup"><span data-stu-id="d06ac-123">The name of the Login to the destination server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d06ac-124"><strong>MotDePasse</strong></span><span class="sxs-lookup"><span data-stu-id="d06ac-124"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ac-p104">Mot de passe de l’argument <strong>Connexion</strong>. Ce mot de passe est stocké sous forme de texte dans le projet Access, mais il est masqué durant l’opération de transfert de base de données.</span><span class="sxs-lookup"><span data-stu-id="d06ac-p104">The password for the <strong>Login</strong> argument. This password is stored as text in the Access project, but is hidden during the transfer database operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d06ac-127"><strong>Transfert des données de copie</strong></span><span class="sxs-lookup"><span data-stu-id="d06ac-127"><strong>Transfer Copy Data</strong></span></span></p></td>
<td><p><span data-ttu-id="d06ac-p105">Spécifie si les données doivent être incluses dans l’opération de transfert de base de données. Si la valeur sélectionnée est <strong>Oui</strong>, toutes les données seront incluses pour toutes les tables, ainsi que les structures de données, les propriétés étendues et les objets de base de données. Si la valeur sélectionnée est <strong>Non</strong>, aucune donnée des tables ne sera incluse. Seules la structure de la table et les propriétés étendues seront créées sur le serveur de destination, ainsi que les objets de base de données, à l’exception toutefois des schémas de bases de données. La valeur par défaut est <strong>Oui</strong>.</span><span class="sxs-lookup"><span data-stu-id="d06ac-p105">Specifies whether or not to include data in the transfer database operation. When set to <strong>Yes</strong>, all data is included for all the tables, along with all data structures, extended properties, and database objects. When set to <strong>No</strong>, no data is included from the tables. Only the table structure and extended properties are created on the destination server, along with all other database objects (except database diagrams). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d06ac-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="d06ac-133">Remarks</span></span>

<span data-ttu-id="d06ac-134">Aucune autre opération n'est autorisée lors du processus de transfert de base de données.</span><span class="sxs-lookup"><span data-stu-id="d06ac-134">You cannot perform other operations while the database is being transferred.</span></span>

<span data-ttu-id="d06ac-135">Par défaut, l'action **TransférerBaseDeDonnéesSQL** copie les données, les définitions de données, les objets de base de données et les propriétés étendues telles que les valeurs par défaut, les contraintes de texte et les valeurs de recherche.</span><span class="sxs-lookup"><span data-stu-id="d06ac-135">The **TransferSQLDatabase** action, by default, copies data, data definitions, database objects, and extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="d06ac-136">Pour pouvoir transférer une base de données, les conditions suivantes doivent être réunies :</span><span class="sxs-lookup"><span data-stu-id="d06ac-136">There are requirements for transferring a database:</span></span>

  - <span data-ttu-id="d06ac-137">Vous devez être membre du rôle sysadmin sur le serveur de destination (aucun rôle spécifique n'est requis sur le serveur source).</span><span class="sxs-lookup"><span data-stu-id="d06ac-137">You must be a member of the sysadmin role on the destination server (No special role is required on the source server).</span></span>

<!-- end list -->

  - <span data-ttu-id="d06ac-138">Le serveur SQL actif, connecté au projet Access et au serveur de destination vers lequel la base de données est transférée doit être un serveur SQL Server version 7.0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d06ac-138">The current SQL server connected to the Access project and the destination server you are transferring the database to must be SQL Server version 7.0 or later.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d06ac-139">[!REMARQUE] Les serveurs liés ne sont pas transférés lors du transfert d'une base de données.</span><span class="sxs-lookup"><span data-stu-id="d06ac-139">Linked servers are not transferred during a database transfer operation.</span></span></P>



<span data-ttu-id="d06ac-140">Pour exécuter l'action **TransférerBaseDeDonnéesSQL** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **TransferSQLDatabase** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="d06ac-140">To run the **TransferSQLDatabase** action in a Visual Basic for Applications (VBA) module, use the **TransferSQLDatabase** method of the **DoCmd** object.</span></span>

