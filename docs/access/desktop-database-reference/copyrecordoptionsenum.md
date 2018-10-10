---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 086694ba4cebd04929416c679318a3235f82e86d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470874"
---
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="e8d1c-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="e8d1c-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="e8d1c-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8d1c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e8d1c-104">Spécifie le fonctionnement de la méthode [CopyRecord](copyrecord-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e8d1c-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8d1c-105">Constant</span><span class="sxs-lookup"><span data-stu-id="e8d1c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e8d1c-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8d1c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e8d1c-107">Description</span><span class="sxs-lookup"><span data-stu-id="e8d1c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8d1c-108"><strong>adCopyAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="e8d1c-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d1c-109">4</span><span class="sxs-lookup"><span data-stu-id="e8d1c-109">4</span></span></p></td>
<td><p><span data-ttu-id="e8d1c-p101">Indique que le fournisseur <em>Source</em> essaye de simuler une copie à l’aide d’opérations de téléchargement et de chargement si cette méthode échoue parce que <em>Destination</em> se trouve sur un serveur différent ou si le fournisseur est différent de celui de la <em>Source</em>. Il est à noter que, selon les fonctions des fournisseurs, les performances peuvent varier, allant jusqu’à la perte de données.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-p101">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>. Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d1c-112"><strong>valeur adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="e8d1c-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d1c-113">2</span><span class="sxs-lookup"><span data-stu-id="e8d1c-113">2</span></span></p></td>
<td><p><span data-ttu-id="e8d1c-p102">Copie le répertoire en cours, mais aucun de ses sous-répertoires, vers l'emplacement de destination. L'opération de copie n'est pas récursive.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-p102">Copies the current directory, but none of its subdirectories, to the destination. The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8d1c-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="e8d1c-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d1c-117">1</span><span class="sxs-lookup"><span data-stu-id="e8d1c-117">1</span></span></p></td>
<td><p><span data-ttu-id="e8d1c-118">Remplace le fichier ou le répertoire si la <em>Destination</em> pointe sur un fichier ou un répertoire existant.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d1c-119"><strong>adCopyUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="e8d1c-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d1c-120">-1</span><span class="sxs-lookup"><span data-stu-id="e8d1c-120">-1</span></span></p></td>
<td><p><span data-ttu-id="e8d1c-p103">Par défaut. Effectue l'opération de copie par défaut : l'opération échoue si le fichier ou le répertoire de destination existe déjà, ou si l'opération effectue une copie récursive.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-p103">Default. Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8d1c-123">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="e8d1c-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="e8d1c-124">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="e8d1c-124">These constants do not have ADO/WFC equivalents.</span></span>

