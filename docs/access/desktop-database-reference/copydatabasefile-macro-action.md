---
title: CopierFichierBaseDeDonnées, action de macro
TOCTitle: CopyDatabaseFile Macro Action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 934a44ee754c403a9ef185537c8af114f1200d82
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862533"
---
# <a name="copydatabasefile-macro-action"></a><span data-ttu-id="5d176-102">CopierFichierBaseDeDonnées, action de macro</span><span class="sxs-lookup"><span data-stu-id="5d176-102">CopyDatabaseFile Macro Action</span></span>


<span data-ttu-id="5d176-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d176-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5d176-104">Utilisez l'action **CopierFichierBaseDeDonnées** pour créer une copie de la base de données Microsoft SQL Server 7.0 (ou version supérieure) active attachée à votre projet Access.</span><span class="sxs-lookup"><span data-stu-id="5d176-104">You can use the **CopyDatabaseFile** action to make a copy of the current Microsoft SQL Server 7.0 or later database connected to your Access project.</span></span> <span data-ttu-id="5d176-105">Access détache la base de données active, puis l’attache au serveur de destination.</span><span class="sxs-lookup"><span data-stu-id="5d176-105">Access detaches the current database and then attaches it to the destination server.</span></span> <span data-ttu-id="5d176-106">Pour plus d'informations sur les procédures permettant de détacher et d'attacher une base de données, voir la documentation de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5d176-106">For more information about detaching and attaching a database, see the SQL Server documentation.</span></span>


> [!NOTE]
> <span data-ttu-id="5d176-p102">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="5d176-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



## <a name="setting"></a><span data-ttu-id="5d176-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d176-109">Setting</span></span>

<span data-ttu-id="5d176-110">L'action **CopierFichierBaseDeDonnées** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="5d176-110">The **CopyDatabaseFile** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d176-111">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="5d176-111">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5d176-112">Description</span><span class="sxs-lookup"><span data-stu-id="5d176-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d176-113"><strong>Nom du fichier de base de données</strong></span><span class="sxs-lookup"><span data-stu-id="5d176-113"><strong>Database File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5d176-p103">Nom du nouveau fichier de données maître. Le chemin d’accès par défaut du fichier est l’emplacement actuel du fichier de projet Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="5d176-p103">The name of the new Master Data File. The default path for the file is the current location of the Access project file (.adp).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d176-116"><strong>Remplacer le fichier existant</strong></span><span class="sxs-lookup"><span data-stu-id="5d176-116"><strong>Overwrite Existing File</strong></span></span></p></td>
<td><p><span data-ttu-id="5d176-p104">Indique si un fichier existant portant le même nom doit ou non être remplacé. Si cet argument est défini sur <strong>Oui</strong> et si le nom de fichier existe déjà, le fichier est remplacé. S’il est défini sur <strong>Non</strong> et si le nom de fichier existe déjà, le fichier n’est pas remplacé et l’action échoue. Si le fichier n’existe pas déjà, ce paramètre est ignoré. La valeur par défaut est <strong>Oui</strong>.</span><span class="sxs-lookup"><span data-stu-id="5d176-p104">Specifies whether or not to replace an existing file with the same name. If set to <strong>Yes</strong> and the filename already exists, the file is overwritten. If set to <strong>No</strong> and the filename already exists, the file is not overwritten and the action fails. If the file does not already exist, this setting is ignored. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d176-122"><strong>Déconnecter tous les utilisateurs</strong></span><span class="sxs-lookup"><span data-stu-id="5d176-122"><strong>Disconnect All Users</strong></span></span></p></td>
<td><p><span data-ttu-id="5d176-p105">Spécifie si Access doit ou non forcer la déconnexion des utilisateurs de la base de données. Si cet argument est défini sur <strong>Oui</strong>, tout utilisateur connecté à la base de données active est déconnecté et l’opération de copie de la base de données peut se poursuivre. S’il est défini sur <strong>Non</strong> et si un ou plusieurs utilisateurs sont connectés à la base de données, l’opération de copie de la base de données échoue. La valeur par défaut est <strong>Non</strong>. 

</span><span class="sxs-lookup"><span data-stu-id="5d176-p105">Specifies whether or not Access should force users off the database. If set to <strong>Yes</strong>, any users that are connected to the current database are disconnected so that the copy database operation can proceed. If set to <strong>No</strong> and one or more users are connected to the database, the copy database operation fails. The default is <strong>No</strong>.</span></span></p>

> [!WARNING]
> <span data-ttu-id="5d176-127">Si les utilisateurs sont déconnectés d’une base de données sans avertissement adéquat, des données risquent d’être perdues.</span><span class="sxs-lookup"><span data-stu-id="5d176-127">Disconnecting users from a database without adequate warning can lead to data loss.</span></span>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5d176-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d176-128">Remarks</span></span>

<span data-ttu-id="5d176-129">L'opération de copie est une opération synchrone. Vous ne pouvez pas réaliser d'autres opérations jusqu'à ce que la copie de la base de données soit terminée.</span><span class="sxs-lookup"><span data-stu-id="5d176-129">The copy operation is synchronous, so you can't perform other operations until the copy of the database is complete.</span></span>

<span data-ttu-id="5d176-130">L'action **CopierFichierBaseDeDonnées** non seulement copie les données, les définitions de données et les objets de base de données, mais aussi les propriétés étendues, comme les valeurs par défaut, les contraintes de texte et les valeurs de recherche.</span><span class="sxs-lookup"><span data-stu-id="5d176-130">The **CopyDatabaseFile** action not only copies data, data definitions, and database objects, but also copies extended properties, such as default values, text constraints, and lookup values.</span></span>

<span data-ttu-id="5d176-131">Conditions requises pour la copie d'une base de données :</span><span class="sxs-lookup"><span data-stu-id="5d176-131">Requirements for copying a database:</span></span>

  - <span data-ttu-id="5d176-132">vous devez déconnecter toutes les applications et tous les utilisateurs avant de copier le fichier de base de données ;</span><span class="sxs-lookup"><span data-stu-id="5d176-132">You must disconnect all applications and users before you copy the database file.</span></span>

  - <span data-ttu-id="5d176-133">tous les objets et toutes les vues, à l'exception du volet de navigation, doivent être fermés ;</span><span class="sxs-lookup"><span data-stu-id="5d176-133">All objects and views except the Navigation Pane must be closed.</span></span>

  - <span data-ttu-id="5d176-134">la base de données active ne doit pas être répliquée ;</span><span class="sxs-lookup"><span data-stu-id="5d176-134">The current database must not be replicated.</span></span>

  - <span data-ttu-id="5d176-135">la base de données serveur source doit être une base de données Microsoft SQL Server 7.0 ou version supérieure ou une base de données SQL Server 2000 Desktop Engine exécutée sur un ordinateur local ;</span><span class="sxs-lookup"><span data-stu-id="5d176-135">The source server database must be Microsoft SQL Server version 7.0 or later, or SQL Server 2000 Desktop Engine running on a local computer.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d176-136">la base de données SQL Server sur le serveur source doit être un base de données à fichier unique ;</span><span class="sxs-lookup"><span data-stu-id="5d176-136">The SQL Server database on the source server must be a single file database.</span></span>

  - <span data-ttu-id="5d176-137">vous devez être membre du rôle sysadmin sur les ordinateurs SQL Server source et de destination.</span><span class="sxs-lookup"><span data-stu-id="5d176-137">You must be a member of the sysadmin role on both the source and destination SQL Server computers.</span></span>

<span data-ttu-id="5d176-138">Pour exécuter l'action **CopierFichierBaseDeDonnées** dans un module Visual Basic pour Applications, utilisez la méthode **CopyDatabaseFile** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="5d176-138">To run the **CopyDatabaseFile** action in a Visual Basic for Applications module, use the **CopyDatabaseFile** method of the **DoCmd** object.</span></span>

