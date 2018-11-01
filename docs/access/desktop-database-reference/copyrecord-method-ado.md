---
title: CopyRecord, méthode (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9daa27f5a5e31aac295babf6f40b32f89a9df5c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874964"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="ad541-102">CopyRecord, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ad541-102">CopyRecord Method (ADO)</span></span>


<span data-ttu-id="ad541-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad541-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad541-104">Copie une entité représentée par un objet **Record** vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="ad541-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad541-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad541-105">Syntax</span></span>

<span data-ttu-id="ad541-106">*Enregistrement*. CopyRecord (*Source*, *Destination*, *nom d’utilisateur*, *mot de passe*, *Options*, *asynchrone*)</span><span class="sxs-lookup"><span data-stu-id="ad541-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="ad541-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad541-107">Parameters</span></span>

  - <span data-ttu-id="ad541-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="ad541-108">*Source*</span></span>

  - <span data-ttu-id="ad541-109">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="ad541-109">Optional.</span></span> <span data-ttu-id="ad541-110">Valeur de type **String** contenant une URL spécifiant l'entité à copier (par exemple, un fichier ou un répertoire).</span><span class="sxs-lookup"><span data-stu-id="ad541-110">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="ad541-111">Si la *Source* est omis ou spécifie une chaîne vide, le fichier ou le répertoire représenté par l' [enregistrement](record-object-ado.md) actif est copié.</span><span class="sxs-lookup"><span data-stu-id="ad541-111">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>

  - <span data-ttu-id="ad541-112">*Destination*</span><span class="sxs-lookup"><span data-stu-id="ad541-112">*Destination*</span></span>

  - <span data-ttu-id="ad541-113">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="ad541-113">Optional.</span></span> <span data-ttu-id="ad541-114">Une valeur de **type String** qui contient une URL spécifiant l’emplacement dans lequel *Source* va être copié.</span><span class="sxs-lookup"><span data-stu-id="ad541-114">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>

  - <span data-ttu-id="ad541-115">*Nom d’utilisateur*</span><span class="sxs-lookup"><span data-stu-id="ad541-115">*UserName*</span></span>

  - <span data-ttu-id="ad541-p103">Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Destination*.</span><span class="sxs-lookup"><span data-stu-id="ad541-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="ad541-118">*MotDePasse*</span><span class="sxs-lookup"><span data-stu-id="ad541-118">*Password*</span></span>

  - <span data-ttu-id="ad541-p104">Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.</span><span class="sxs-lookup"><span data-stu-id="ad541-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="ad541-121">*Options*</span><span class="sxs-lookup"><span data-stu-id="ad541-121">*Options*</span></span>

  - <span data-ttu-id="ad541-p105">Facultatif. Valeur de l'énumération [CopyRecordOptionsEnum](copyrecordoptionsenum.md) (par défaut, **adCopyUnspecified** ). Spécifie le comportement de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ad541-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="ad541-125">*Async*</span><span class="sxs-lookup"><span data-stu-id="ad541-125">*Async*</span></span>

  - <span data-ttu-id="ad541-p106">Facultatif. Valeur de type **Boolean** qui, lorsqu'elle correspond à **True**, indique que cette opération doit être asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ad541-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad541-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ad541-128">Return value</span></span>

<span data-ttu-id="ad541-p107">Valeur de type **String** qui retourne, en général, la valeur de *Destination*. Toutefois, la valeur exacte renvoyée dépend du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ad541-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad541-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="ad541-131">Remarks</span></span>

<span data-ttu-id="ad541-132">Les valeurs de la *Source* et de *Destination* ne doivent pas être identiques ; dans le cas contraire, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="ad541-132">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="ad541-133">Il faut au moins que le nom du serveur, du chemin d'accès ou de la ressource diffère.</span><span class="sxs-lookup"><span data-stu-id="ad541-133">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="ad541-p109">Tous les enfants (par exemple, les sous-répertoires) de *Source* sont copiés de manière récursive sauf si la valeur **adCopyNonRecursive** est spécifiée. Dans une opération récursive, *Destination* ne doit pas correspondre à un sous-répertoire de *Source* sans quoi l'opération n'est pas exécutée.</span><span class="sxs-lookup"><span data-stu-id="ad541-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="ad541-136">Cette méthode échoue si *Destination* identifie une entité existante (par exemple, un fichier ou un répertoire) sauf si **adCopyOverWrite** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="ad541-136">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="ad541-137">[!IMPORTANTE] Soyez prudent lorsque vous utilisez l'option **adCopyOverWrite**.</span><span class="sxs-lookup"><span data-stu-id="ad541-137">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="ad541-138">Par exemple, si cette option lors de la copie d’un fichier dans un répertoire sera *Supprimer* le répertoire et remplacez-la par le fichier.</span><span class="sxs-lookup"><span data-stu-id="ad541-138">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>




> [!NOTE]
> <span data-ttu-id="ad541-139">[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="ad541-139">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="ad541-140">Pour plus d’informations, consultez [URL absolues et relatives](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="ad541-140">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


