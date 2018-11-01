---
title: DBEngine Members (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2763825fa3e182d2007be65a88e18988699f26f8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891161"
---
# <a name="dbengine-members-dao"></a><span data-ttu-id="72fb1-102">DBEngine Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="72fb1-102">DBEngine Members (DAO)</span></span>


<span data-ttu-id="72fb1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72fb1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72fb1-104">L'objet DBEngine est l'objet de niveau supérieur dans le modèle objet DAO.</span><span class="sxs-lookup"><span data-stu-id="72fb1-104">The DBEngine object is the top level object in the DAO object model.</span></span>

## <a name="methods"></a><span data-ttu-id="72fb1-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="72fb1-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72fb1-106">Nom</span><span class="sxs-lookup"><span data-stu-id="72fb1-106">Name</span></span></p></th>
<th><p><span data-ttu-id="72fb1-107">Description</span><span class="sxs-lookup"><span data-stu-id="72fb1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-108"><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-p101">Commence une nouvelle transaction. <strong>Database</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="72fb1-p101">Begins a new transaction. Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72fb1-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-111"><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-112">Met fin à la transaction en cours et enregistre les modifications.</span><span class="sxs-lookup"><span data-stu-id="72fb1-112">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-113"><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-p102">Copie et compacte une base de données fermée et offre la possibilité d'en modifier la version, l'ordre de classement et le chiffrement. (Pour les espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="72fb1-p102">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption. (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72fb1-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-117"><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-p103">Crée un objet <strong><a href="database-object-dao.md">Database</a></strong>, enregistre la base de données sur le disque, et renvoie un objet <strong>Database</strong> ouvert (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="72fb1-p103">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-120"><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-121">Crée un nouvel objet <strong><a href="workspace-object-dao.md">Workspace</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="72fb1-121">Creates a new <strong><a href="workspace-object-dao.md">Workspace</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72fb1-122"><strong><a href="dbengine-idle-method-dao.md">Inactif</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-122"><strong><a href="dbengine-idle-method-dao.md">Idle</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-123">Suspend le traitement des données, ce qui permet au moteur de base de données Microsoft Access de terminer les tâches en cours, telles que l'optimisation de la mémoire ou les expirations de délai des pages (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="72fb1-123">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-124"><strong><a href="dbengine-openconnection-method-dao.md">Méthode OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-124"><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="72fb1-p104">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="72fb1-p104">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="72fb1-127">Ouvre un objet <strong><a href="connection-object-dao.md">Connection</a></strong> dans une source de données ODBC (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="72fb1-127">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72fb1-128"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-128"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-129">Ouvre une base de données spécifiée et renvoie une référence à l'objet <strong><a href="database-object-dao.md">Database</a></strong> qui la représente.</span><span class="sxs-lookup"><span data-stu-id="72fb1-129">Opens a specified database and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-130"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-130"><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-p105">Entre les informations de connexion pour une source de données ODBC dans le Registre Windows. Le pilote ODBC a besoin des informations de connexion lorsque la source de données ODBC est ouverte au cours d'une session.</span><span class="sxs-lookup"><span data-stu-id="72fb1-p105">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72fb1-133"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-133"><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-134">Met fin à transaction en cours et restaure les bases de données dans l'objet <strong>Workspace</strong> à l'état dans lequel elles se trouvaient au début de la transaction actuelle.</span><span class="sxs-lookup"><span data-stu-id="72fb1-134">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-135"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-135"><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-136">Remplace temporairement les valeurs des clés du moteur de base de données Microsoft Access dans le registre Windows (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="72fb1-136">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="72fb1-137">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72fb1-137">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72fb1-138">Nom</span><span class="sxs-lookup"><span data-stu-id="72fb1-138">Name</span></span></p></th>
<th><p><span data-ttu-id="72fb1-139">Description</span><span class="sxs-lookup"><span data-stu-id="72fb1-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-140"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-140"><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-p106">Définit le mot de passe servant à créer l'objet <strong>Workspace</strong> par défaut lors de son initialisation. Valeur de type <strong>String</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="72fb1-p106">Sets the password used to create the default <strong>Workspace</strong> when it is initialized. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72fb1-143"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-143"><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-144">Définit ou renvoie une valeur qui indique le type d'espace de travail qui sera utilisé par le prochain objet <strong><a href="workspace-object-dao.md">Workspace</a></strong> créé.</span><span class="sxs-lookup"><span data-stu-id="72fb1-144">Sets or returns a value that indicates what type of workspace will be used by the next <strong><a href="workspace-object-dao.md">Workspace</a></strong> object created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-145"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-145"><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-p107">Définit le nom d'utilisateur servant à créer l'objet <strong>Workspace</strong> par défaut lors de son initialisation. Valeur de type <strong>String</strong> en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="72fb1-p107">Sets the user name used to create the default <strong>Workspace</strong> when it is initialized. Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72fb1-148"><strong><a href="dbengine-errors-property-dao.md">Erreurs</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-148"><strong><a href="dbengine-errors-property-dao.md">Errors</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-p108">Renvoie une collection <strong>Errors</strong> qui contient tous les objets <strong>Error</strong> enregistrés pour l'objet spécifié. Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="72fb1-p108">Returns an <strong>Errors</strong> collection that contains all of the stored <strong>Error</strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-151"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-151"><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-152">Définit ou renvoie des informations sur la clé du Registre Windows contenant les valeurs relatives au moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="72fb1-152">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72fb1-153"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-153"><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-154">Définit ou renvoie le nombre de secondes devant s'écouler avant l'apparition d'une erreur lorsque vous essayez de vous connecter à une base de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="72fb1-154">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-155"><strong><a href="dbengine-properties-property-dao.md">Propriétés</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-155"><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-p109">Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</span><span class="sxs-lookup"><span data-stu-id="72fb1-p109">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72fb1-158"><strong><a href="dbengine-version-property-dao.md">Version</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-158"><strong><a href="dbengine-version-property-dao.md">Version</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-p110">Renvoie la version de DAO en cours d'utilisation. Valeur de type <strong>String</strong> en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="72fb1-p110">Rreturns the version of DAO currently in use. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72fb1-161"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span><span class="sxs-lookup"><span data-stu-id="72fb1-161"><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></span></span></p></td>
<td><p><span data-ttu-id="72fb1-p111">Renvoie une collection <strong>Workspaces</strong> qui contient tous les objets <strong>Workspace</strong> actifs et non masqués. Valeur en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="72fb1-p111">Returns a <strong>Workspaces</strong> collection that contains all of the active, unhidden <strong>Workspace</strong> objects. Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

