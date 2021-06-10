---
title: CopyRecord, méthode (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295526"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="e89be-102">CopyRecord, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="e89be-102">CopyRecord method (ADO)</span></span>

<span data-ttu-id="e89be-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e89be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e89be-104">Copie une entité représentée par un objet **Record** vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="e89be-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="e89be-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e89be-105">Syntax</span></span>

<span data-ttu-id="e89be-106">*Enregistrement*. CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="e89be-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="e89be-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e89be-107">Parameters</span></span>

|<span data-ttu-id="e89be-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e89be-108">Parameter</span></span>|<span data-ttu-id="e89be-109">Description</span><span class="sxs-lookup"><span data-stu-id="e89be-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e89be-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="e89be-110">*Source*</span></span> |<span data-ttu-id="e89be-p101">Facultatif. Valeur de type **String** contenant une URL spécifiant l’entité à copier (par exemple, un fichier ou un répertoire). Si le paramètre *Source* est omis ou spécifie une chaîne vide, le fichier ou le répertoire représenté par l’objet [Record](record-object-ado.md) actif est copié.</span><span class="sxs-lookup"><span data-stu-id="e89be-p101">Optional. A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory). If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>|
|<span data-ttu-id="e89be-114">*Destination*</span><span class="sxs-lookup"><span data-stu-id="e89be-114">*Destination*</span></span> |<span data-ttu-id="e89be-p102">Facultatif. Valeur de type **String** contenant une URL spécifiant l'emplacement dans lequel *Source* va être copié.</span><span class="sxs-lookup"><span data-stu-id="e89be-p102">Optional. A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>|
|<span data-ttu-id="e89be-117">*UserName*</span><span class="sxs-lookup"><span data-stu-id="e89be-117">*UserName*</span></span> |<span data-ttu-id="e89be-p103">Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Destination*.</span><span class="sxs-lookup"><span data-stu-id="e89be-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="e89be-120">*Password*</span><span class="sxs-lookup"><span data-stu-id="e89be-120">*Password*</span></span> |<span data-ttu-id="e89be-p104">Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.</span><span class="sxs-lookup"><span data-stu-id="e89be-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="e89be-123">*Options*</span><span class="sxs-lookup"><span data-stu-id="e89be-123">*Options*</span></span> |<span data-ttu-id="e89be-p105">Facultatif. Valeur de l'énumération [CopyRecordOptionsEnum](copyrecordoptionsenum.md) (par défaut, **adCopyUnspecified** ). Spécifie le comportement de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="e89be-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="e89be-127">*Async*</span><span class="sxs-lookup"><span data-stu-id="e89be-127">*Async*</span></span> |<span data-ttu-id="e89be-p106">Facultatif. Valeur de type **Boolean** qui, lorsqu'elle correspond à **True**, indique que cette opération doit être asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e89be-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="e89be-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e89be-130">Return value</span></span>

<span data-ttu-id="e89be-p107">Valeur de type **String** qui retourne, en général, la valeur de *Destination*. Toutefois, la valeur exacte renvoyée dépend du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e89be-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="e89be-133">Remarques</span><span class="sxs-lookup"><span data-stu-id="e89be-133">Remarks</span></span>

<span data-ttu-id="e89be-p108">Les valeurs des paramètres *Source* et *Destination* ne doivent pas être identiques sans quoi une erreur d'exécution se produit. Il faut au moins que le nom du serveur, du chemin d'accès ou de la ressource diffère.</span><span class="sxs-lookup"><span data-stu-id="e89be-p108">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs. At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="e89be-p109">Tous les enfants (par exemple, les sous-répertoires) de *Source* sont copiés de manière récursive sauf si la valeur **adCopyNonRecursive** est spécifiée. Dans une opération récursive, *Destination* ne doit pas correspondre à un sous-répertoire de *Source* sans quoi l'opération n'est pas exécutée.</span><span class="sxs-lookup"><span data-stu-id="e89be-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="e89be-138">Cette méthode échoue si *Destination* identifie une entité existante (par exemple, un fichier ou un répertoire) sauf si **adCopyOverWrite** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="e89be-138">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e89be-p110">Soyez prudent lorsque vous utilisez l'option **adCopyOverWrite**. Si, par exemple, vous la spécifiez lors de la copie d'un fichier dans un répertoire, ce répertoire est *supprimé* et remplacé par le fichier.</span><span class="sxs-lookup"><span data-stu-id="e89be-p110">Use the **adCopyOverWrite** option judiciously. For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>


> [!NOTE]
> <span data-ttu-id="e89be-141">Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="e89be-141">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="e89be-142">Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="e89be-142">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


