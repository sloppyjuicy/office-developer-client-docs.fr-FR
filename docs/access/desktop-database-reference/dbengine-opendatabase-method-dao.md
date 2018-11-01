---
title: Méthode DBEngine.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 45075a612b5d8dc6fabd4a91cc1efdacf37874a0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878940"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="67b90-102">Méthode DBEngine.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="67b90-102">DBEngine.OpenDatabase Method (DAO)</span></span>


<span data-ttu-id="67b90-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67b90-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67b90-104">Ouvre une base de données spécifiée et renvoie une référence à l'objet **[Database](database-object-dao.md)** qui la représente.</span><span class="sxs-lookup"><span data-stu-id="67b90-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="67b90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67b90-105">Syntax</span></span>

<span data-ttu-id="67b90-106">*expression* . OpenDatabase (***nom***, ***Options***, ***ReadOnly***, ***connecter***)</span><span class="sxs-lookup"><span data-stu-id="67b90-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="67b90-107">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="67b90-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="67b90-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67b90-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67b90-109">Name</span><span class="sxs-lookup"><span data-stu-id="67b90-109">Name</span></span></p></th>
<th><p><span data-ttu-id="67b90-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="67b90-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="67b90-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="67b90-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="67b90-112">Description</span><span class="sxs-lookup"><span data-stu-id="67b90-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67b90-113">Name</span><span class="sxs-lookup"><span data-stu-id="67b90-113">Name</span></span></p></td>
<td><p><span data-ttu-id="67b90-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="67b90-114">Required</span></span></p></td>
<td><p><span data-ttu-id="67b90-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="67b90-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="67b90-p101">Nom d'un fichier de base de données Microsoft Access existant ou nom de source de données (DSN) d'une source de données ODBC. Consultez la propriété <strong><a href="connection-name-property-dao.md">Name</a></strong> pour obtenir plus d'informations sur la définition de cette valeur.  </span><span class="sxs-lookup"><span data-stu-id="67b90-p101">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67b90-118">Options</span><span class="sxs-lookup"><span data-stu-id="67b90-118">Options</span></span></p></td>
<td><p><span data-ttu-id="67b90-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="67b90-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="67b90-120"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="67b90-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="67b90-121">Définit différentes options pour la base de données, selon les indications dans les notes.</span><span class="sxs-lookup"><span data-stu-id="67b90-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67b90-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="67b90-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="67b90-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="67b90-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="67b90-124"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="67b90-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="67b90-125"><strong>True</strong> si vous souhaitez ouvrir la base de données avec un accès en lecture seule, ou <strong>False</strong> (valeur par défaut) si vous souhaitez ouvrir la base de données avec un accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="67b90-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67b90-126">Connexion</span><span class="sxs-lookup"><span data-stu-id="67b90-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="67b90-127">Facultatif</span><span class="sxs-lookup"><span data-stu-id="67b90-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="67b90-128"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="67b90-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="67b90-129">Spécifie les différentes informations de connexion, dont les mots de passe.</span><span class="sxs-lookup"><span data-stu-id="67b90-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="67b90-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="67b90-130">Return value</span></span>

<span data-ttu-id="67b90-131">Base de données</span><span class="sxs-lookup"><span data-stu-id="67b90-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="67b90-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="67b90-132">Remarks</span></span>

<span data-ttu-id="67b90-133">Vous pouvez utiliser les valeurs ci-dessous pour l'argument options.</span><span class="sxs-lookup"><span data-stu-id="67b90-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67b90-134">Paramètre</span><span class="sxs-lookup"><span data-stu-id="67b90-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="67b90-135">Description</span><span class="sxs-lookup"><span data-stu-id="67b90-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67b90-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="67b90-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="67b90-137">Ouvre la base de données en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="67b90-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67b90-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="67b90-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="67b90-139">(Valeur par défaut) Ouvre la base de données en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="67b90-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="67b90-140">Lorsque vous ouvrez une base de données, elle est automatiquement ajoutée à la collection **Databases**.</span><span class="sxs-lookup"><span data-stu-id="67b90-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="67b90-141">Certaines considérations s’appliquent lorsque vous utilisez NomBaseDonnées :</span><span class="sxs-lookup"><span data-stu-id="67b90-141">Some considerations apply when you use dbname:</span></span>

  - <span data-ttu-id="67b90-142">S'il s'agit d'une base de données déjà ouverte pour un accès par un autre utilisateur, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="67b90-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

  - <span data-ttu-id="67b90-143">S'il ne s'agit pas d'une base de données existante ou d'un nom de source de données ODBC valide, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="67b90-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

  - <span data-ttu-id="67b90-144">S’il s’agit d’une chaîne de longueur nulle (« ») et *vous connecter* est « ODBC ; », une boîte de dialogue répertoriant les noms de source de données ODBC tous enregistrés s’affiche afin que l’utilisateur peut sélectionner une base de données.</span><span class="sxs-lookup"><span data-stu-id="67b90-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="67b90-145">Pour fermer une base de données, et ainsi supprimer l'objet **Database** de la collection **Databases**, utilisez la méthode **[Close](connection-close-method-dao.md)** dans l'objet.</span><span class="sxs-lookup"><span data-stu-id="67b90-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>


> [!NOTE]
> <span data-ttu-id="67b90-146">[!REMARQUE] Lorsque vous accédez à une source de données ODBC connectée au moteur de base de données Microsoft Access, vous pouvez améliorer les performances de votre application en ouvrant un objet **Database** connecté à la source de données ODBC, ce qui vous évite de lier des objets [TableDef](tabledef-object-dao.md) individuels à des tables spécifiques dans la source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="67b90-146">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


