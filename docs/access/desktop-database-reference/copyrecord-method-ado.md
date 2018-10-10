---
title: CopyRecord, méthode (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a54cf5f4d14b3e623a576dee99e1fabeb070e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470836"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="7121f-102">CopyRecord, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="7121f-102">CopyRecord Method (ADO)</span></span>


<span data-ttu-id="7121f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7121f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7121f-104">Copie une entité représentée par un objet **Record** vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="7121f-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="7121f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7121f-105">Syntax</span></span>

<span data-ttu-id="7121f-106">*Enregistrement*. CopyRecord (*Source*, *Destination*, *nom d’utilisateur*, *mot de passe*, *Options*, *asynchrone*)</span><span class="sxs-lookup"><span data-stu-id="7121f-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="7121f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7121f-107">Parameters</span></span>

  - <span data-ttu-id="7121f-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="7121f-108">*Source*</span></span>

  - <span data-ttu-id="7121f-109">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="7121f-109">Optional.</span></span> <span data-ttu-id="7121f-110">Valeur de type **String** contenant une URL spécifiant l'entité à copier (par exemple, un fichier ou un répertoire).</span><span class="sxs-lookup"><span data-stu-id="7121f-110">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="7121f-111">Si la *Source* est omis ou spécifie une chaîne vide, le fichier ou le répertoire représenté par l' [enregistrement](record-object-ado.md) actif est copié.</span><span class="sxs-lookup"><span data-stu-id="7121f-111">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>

  - <span data-ttu-id="7121f-112">*Destination*</span><span class="sxs-lookup"><span data-stu-id="7121f-112">*Destination*</span></span>

  - <span data-ttu-id="7121f-113">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="7121f-113">Optional.</span></span> <span data-ttu-id="7121f-114">Une valeur de **type String** qui contient une URL spécifiant l’emplacement dans lequel *Source* va être copié.</span><span class="sxs-lookup"><span data-stu-id="7121f-114">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>

  - <span data-ttu-id="7121f-115">*Nom d’utilisateur*</span><span class="sxs-lookup"><span data-stu-id="7121f-115">*UserName*</span></span>

  - <span data-ttu-id="7121f-p103">Facultatif. Valeur de type **String** contenant l'ID utilisateur, qui le cas échéant, autorise l'accès à *Destination*.</span><span class="sxs-lookup"><span data-stu-id="7121f-p103">Optional. A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="7121f-118">*MotDePasse*</span><span class="sxs-lookup"><span data-stu-id="7121f-118">*Password*</span></span>

  - <span data-ttu-id="7121f-p104">Facultatif. Valeur de type **String** contenant le mot de passe qui, le cas échéant, vérifie le paramètre *NomUtilisateur*.</span><span class="sxs-lookup"><span data-stu-id="7121f-p104">Optional. A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="7121f-121">*Options*</span><span class="sxs-lookup"><span data-stu-id="7121f-121">*Options*</span></span>

  - <span data-ttu-id="7121f-p105">Facultatif. Valeur de l'énumération [CopyRecordOptionsEnum](copyrecordoptionsenum.md) (par défaut, **adCopyUnspecified** ). Spécifie le comportement de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7121f-p105">Optional. A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**. Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="7121f-125">*Async*</span><span class="sxs-lookup"><span data-stu-id="7121f-125">*Async*</span></span>

  - <span data-ttu-id="7121f-p106">Facultatif. Valeur de type **Boolean** qui, lorsqu'elle correspond à **True**, indique que cette opération doit être asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7121f-p106">Optional. A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>

## <a name="return-value"></a><span data-ttu-id="7121f-128">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7121f-128">Return Value</span></span>

<span data-ttu-id="7121f-p107">Valeur de type **String** qui retourne, en général, la valeur de *Destination*. Toutefois, la valeur exacte renvoyée dépend du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7121f-p107">A **String** value that typically returns the value of *Destination*. However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="7121f-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="7121f-131">Remarks</span></span>

<span data-ttu-id="7121f-132">Les valeurs de la *Source* et de *Destination* ne doivent pas être identiques ; dans le cas contraire, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="7121f-132">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="7121f-133">Il faut au moins que le nom du serveur, du chemin d'accès ou de la ressource diffère.</span><span class="sxs-lookup"><span data-stu-id="7121f-133">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="7121f-p109">Tous les enfants (par exemple, les sous-répertoires) de *Source* sont copiés de manière récursive sauf si la valeur **adCopyNonRecursive** est spécifiée. Dans une opération récursive, *Destination* ne doit pas correspondre à un sous-répertoire de *Source* sans quoi l'opération n'est pas exécutée.</span><span class="sxs-lookup"><span data-stu-id="7121f-p109">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified. In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="7121f-136">Cette méthode échoue si *Destination* identifie une entité existante (par exemple, un fichier ou un répertoire) sauf si **adCopyOverWrite** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="7121f-136">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>


> [!IMPORTANT]
> <P><span data-ttu-id="7121f-137">[!IMPORTANTE] Soyez prudent lorsque vous utilisez l'option <STRONG>adCopyOverWrite</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7121f-137">Use the <STRONG>adCopyOverWrite</STRONG> option judiciously.</span></span> <span data-ttu-id="7121f-138">Par exemple, si cette option lors de la copie d’un fichier dans un répertoire sera <EM>Supprimer</EM> le répertoire et remplacez-la par le fichier.</span><span class="sxs-lookup"><span data-stu-id="7121f-138">For example, specifying this option when copying a file to a directory will <EM>delete</EM> the directory and replace it with the file.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="7121f-p111">[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, consultez <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</span><span class="sxs-lookup"><span data-stu-id="7121f-p111">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


