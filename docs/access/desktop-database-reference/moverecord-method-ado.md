---
title: MoveRecord, méthode (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5aab77571b0b12c6b26cd15af386c9ee89162681
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930013"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="35eb1-102">MoveRecord, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="35eb1-102">MoveRecord method (ADO)</span></span>


<span data-ttu-id="35eb1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="35eb1-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="35eb1-104">Déplace l'entité représentée par un objet [Record](record-object-ado.md) vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="35eb1-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="35eb1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35eb1-105">Syntax</span></span>

<span data-ttu-id="35eb1-106">*Enregistrement*. MoveRecord (*Source*, *Destination*, *nom d’utilisateur*, *mot de passe*, *Options*, *asynchrone*)</span><span class="sxs-lookup"><span data-stu-id="35eb1-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="35eb1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35eb1-107">Parameters</span></span>

  - <span data-ttu-id="35eb1-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="35eb1-108">*Source*</span></span>

  - <span data-ttu-id="35eb1-p101">Facultatif. Valeur de type **String** qui contient une URL identifiant l'objet **Record** à déplacer. Si *Source* est omis ou spécifie une chaîne vide, l'objet représenté par cet **enregistrement** est déplacé. Par exemple si l'objet **Record** représente un fichier, le contenu du fichier est déplacé vers l'emplacement spécifié par le paramètre *Destination*.</span><span class="sxs-lookup"><span data-stu-id="35eb1-p101">Optional. A **String** value that contains a URL identifying the **Record** to be moved. If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved. For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>

  - <span data-ttu-id="35eb1-113">*Destination*</span><span class="sxs-lookup"><span data-stu-id="35eb1-113">*Destination*</span></span>

  - <span data-ttu-id="35eb1-114">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="35eb1-114">Optional.</span></span> <span data-ttu-id="35eb1-115">Une valeur de **type String** qui contient une URL spécifiant l’emplacement où seront déplacées *Source* .</span><span class="sxs-lookup"><span data-stu-id="35eb1-115">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>

  - <span data-ttu-id="35eb1-116">*Nom d’utilisateur*</span><span class="sxs-lookup"><span data-stu-id="35eb1-116">*UserName*</span></span>

  - <span data-ttu-id="35eb1-p103">Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Destination*.</span><span class="sxs-lookup"><span data-stu-id="35eb1-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="35eb1-119">*MotDePasse*</span><span class="sxs-lookup"><span data-stu-id="35eb1-119">*Password*</span></span>

  - <span data-ttu-id="35eb1-p104">Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.</span><span class="sxs-lookup"><span data-stu-id="35eb1-p104">Optional. A **String** that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="35eb1-122">*Options*</span><span class="sxs-lookup"><span data-stu-id="35eb1-122">*Options*</span></span>

  - <span data-ttu-id="35eb1-p105">Facultatif. Valeur [MoveRecordOptionsEnum](moverecordoptionsenum.md) dont la valeur par défaut est **adMoveUnspecified**. Spécifie le comportement de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="35eb1-p105">Optional. A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="35eb1-126">*Async*</span><span class="sxs-lookup"><span data-stu-id="35eb1-126">*Async*</span></span>

  - <span data-ttu-id="35eb1-p106">Facultatif. Valeur de type **Boolean** qui, lorsqu'elle correspond à **True**, indique que cette opération doit être asynchrone.</span><span class="sxs-lookup"><span data-stu-id="35eb1-p106">Optional. A **Boolean** value that, when **True**, specifies this operation should be asynchronous .</span></span>

## <a name="return-value"></a><span data-ttu-id="35eb1-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="35eb1-129">Return value</span></span>

<span data-ttu-id="35eb1-130">Valeur de type **String**.</span><span class="sxs-lookup"><span data-stu-id="35eb1-130">A **String** value.</span></span> <span data-ttu-id="35eb1-131">En règle générale, la valeur de *Destination* est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="35eb1-131">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="35eb1-132">Toutefois, la valeur retournée précise dépend du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="35eb1-132">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="35eb1-133">Notes</span><span class="sxs-lookup"><span data-stu-id="35eb1-133">Remarks</span></span>

<span data-ttu-id="35eb1-134">Les valeurs de la *Source* et de *Destination* ne doivent pas être identiques ; dans le cas contraire, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="35eb1-134">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="35eb1-135">Il faut au moins que les noms de ressource, de chemin d'accès et de serveur diffèrent.</span><span class="sxs-lookup"><span data-stu-id="35eb1-135">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="35eb1-p109">Pour les fichiers déplacés à l'aide du fournisseur de la publication Internet, cette méthode met à jour tous les liens hypertexte dans les fichiers déplacés sauf indication contraire précisée dans *Options*. Cette méthode échoue si *Destination* identifie un objet existant (fichier ou répertoire, par exemple), à moins que **adMoveOverWrite** soit spécifié.</span><span class="sxs-lookup"><span data-stu-id="35eb1-p109">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*. This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>


> [!NOTE]
> <P><span data-ttu-id="35eb1-p110">[!REMARQUE] Soyez prudent lorsque vous utilisez l'option <STRONG>adMoveOverWrite</STRONG>. Si, par exemple, vous spécifiez cette option lorsque vous déplacez un fichier vers un répertoire, le répertoire est supprimé et remplacé par le fichier.</span><span class="sxs-lookup"><span data-stu-id="35eb1-p110">Use the <STRONG>adMoveOverWrite</STRONG> option judiciously. For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span></P>



<span data-ttu-id="35eb1-140">Certains attributs de l’objet **Record** , telles que la propriété [ParentURL](parenturl-property-ado.md) , ne seront pas mis à jour une fois cette opération terminée.</span><span class="sxs-lookup"><span data-stu-id="35eb1-140">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes.</span></span> <span data-ttu-id="35eb1-141">Actualiser les propriétés de l’objet **Record** en fermant l' **enregistrement**, puis rouvrir avec l’URL de l’emplacement où le fichier ou répertoire a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="35eb1-141">Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="35eb1-p112">Si l'objet **Record** a été obtenu d'un objet [Recordset](recordset-object-ado.md), le nouvel emplacement du fichier ou répertoire déplacé n'est pas directement reflété dans l'objet **Recordset**. Actualisez l'objet **Recordset** en le fermant puis en le rouvrant.</span><span class="sxs-lookup"><span data-stu-id="35eb1-p112">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**. Refresh the **Recordset** by closing and re-opening it.</span></span>


> [!NOTE]
> <span data-ttu-id="35eb1-144">[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="35eb1-144">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="35eb1-145">Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="35eb1-145">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


