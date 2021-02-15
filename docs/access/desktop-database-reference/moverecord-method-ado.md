---
title: MoveRecord, méthode (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9937f0ab32c5dba0e4435fdc0ba7e111f5651dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288678"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="291ef-102">MoveRecord, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="291ef-102">MoveRecord method (ADO)</span></span>

<span data-ttu-id="291ef-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="291ef-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="291ef-104">Déplace l’entité représentée par un objet [Record](record-object-ado.md) vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="291ef-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="291ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="291ef-105">Syntax</span></span>

<span data-ttu-id="291ef-106">*Enregistrement*. MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="291ef-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="291ef-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="291ef-107">Parameters</span></span>

|<span data-ttu-id="291ef-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="291ef-108">Parameter</span></span>|<span data-ttu-id="291ef-109">Description</span><span class="sxs-lookup"><span data-stu-id="291ef-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="291ef-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="291ef-110">*Source*</span></span> |<span data-ttu-id="291ef-p101">Facultatif. Valeur de type **String** qui contient une URL identifiant l'objet **Record** à déplacer. Si *Source* est omis ou spécifie une chaîne vide, l'objet représenté par cet **enregistrement** est déplacé. Par exemple si l'objet **Record** représente un fichier, le contenu du fichier est déplacé vers l'emplacement spécifié par le paramètre *Destination*.</span><span class="sxs-lookup"><span data-stu-id="291ef-p101">Optional. A **String** value that contains a URL identifying the **Record** to be moved. If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved. For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>|
|<span data-ttu-id="291ef-115">*Destination*</span><span class="sxs-lookup"><span data-stu-id="291ef-115">*Destination*</span></span> |<span data-ttu-id="291ef-116">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="291ef-116">Optional.</span></span> <span data-ttu-id="291ef-117">Valeur de type **String** qui contient une URL spécifiant l'emplacement vers lequel déplacer *Source*.</span><span class="sxs-lookup"><span data-stu-id="291ef-117">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>|
|<span data-ttu-id="291ef-118">*UserName*</span><span class="sxs-lookup"><span data-stu-id="291ef-118">*UserName*</span></span> |<span data-ttu-id="291ef-119">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="291ef-119">Optional.</span></span> <span data-ttu-id="291ef-120">Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Destination*.</span><span class="sxs-lookup"><span data-stu-id="291ef-120">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="291ef-121">*Password*</span><span class="sxs-lookup"><span data-stu-id="291ef-121">*Password*</span></span> |<span data-ttu-id="291ef-122">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="291ef-122">Optional.</span></span> <span data-ttu-id="291ef-123">Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.</span><span class="sxs-lookup"><span data-stu-id="291ef-123">A **String** that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="291ef-124">*Options*</span><span class="sxs-lookup"><span data-stu-id="291ef-124">*Options*</span></span> |<span data-ttu-id="291ef-p105">Facultatif. Valeur [MoveRecordOptionsEnum](moverecordoptionsenum.md) dont la valeur par défaut est **adMoveUnspecified**. Spécifie le comportement de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="291ef-p105">Optional. A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="291ef-128">*Async*</span><span class="sxs-lookup"><span data-stu-id="291ef-128">*Async*</span></span> |<span data-ttu-id="291ef-129">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="291ef-129">Optional.</span></span> <span data-ttu-id="291ef-130">Valeur **boolénaire** qui, lorsque la valeur **est True,** spécifie que cette opération doit être asynchrone.</span><span class="sxs-lookup"><span data-stu-id="291ef-130">A **Boolean** value that, when **True**, specifies this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="291ef-131">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="291ef-131">Return value</span></span>

<span data-ttu-id="291ef-132">Valeur de type **String**.</span><span class="sxs-lookup"><span data-stu-id="291ef-132">A **String** value.</span></span> <span data-ttu-id="291ef-133">En général, il s'agit de la valeur de *Destination*.</span><span class="sxs-lookup"><span data-stu-id="291ef-133">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="291ef-134">Toutefois, la valeur retournée précise dépend du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="291ef-134">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="291ef-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="291ef-135">Remarks</span></span>

<span data-ttu-id="291ef-p108">Les valeurs de *Source* et *Destination* ne peuvent pas être identiques sans quoi une erreur d'exécution se produit. Il faut au moins que les noms de ressource, de chemin d'accès et de serveur diffèrent.</span><span class="sxs-lookup"><span data-stu-id="291ef-p108">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs. At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="291ef-p109">Pour les fichiers déplacés à l'aide du fournisseur de la publication Internet, cette méthode met à jour tous les liens hypertexte dans les fichiers déplacés sauf indication contraire précisée dans *Options*. Cette méthode échoue si *Destination* identifie un objet existant (fichier ou répertoire, par exemple), à moins que **adMoveOverWrite** soit spécifié.</span><span class="sxs-lookup"><span data-stu-id="291ef-p109">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*. This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>

> [!NOTE]
> <span data-ttu-id="291ef-p110">[!REMARQUE] Soyez prudent lorsque vous utilisez l'option **adMoveOverWrite**. Si, par exemple, vous spécifiez cette option lorsque vous déplacez un fichier vers un répertoire, le répertoire est supprimé et remplacé par le fichier.</span><span class="sxs-lookup"><span data-stu-id="291ef-p110">Use the **adMoveOverWrite** option judiciously. For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span>

<span data-ttu-id="291ef-p111">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span><span class="sxs-lookup"><span data-stu-id="291ef-p111">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes. Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="291ef-p112">Si l’objet **Record** a été obtenu d’un objet [Recordset](recordset-object-ado.md), le nouvel emplacement du fichier ou répertoire déplacé n’est pas directement reflété dans l’objet **Recordset**. Actualisez l’objet **Recordset** en le fermant puis en le rouvrant.</span><span class="sxs-lookup"><span data-stu-id="291ef-p112">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**. Refresh the **Recordset** by closing and re-opening it.</span></span>

> [!NOTE]
> <span data-ttu-id="291ef-146">Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="291ef-146">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="291ef-147">Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="291ef-147">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


