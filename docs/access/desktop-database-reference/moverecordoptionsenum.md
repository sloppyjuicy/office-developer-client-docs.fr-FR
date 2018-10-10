---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41ec6eaf39545bf8a71f443a8e3b90052a74f1de
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472018"
---
# <a name="moverecordoptionsenum"></a><span data-ttu-id="16cbe-102">MoveRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="16cbe-102">MoveRecordOptionsEnum</span></span>


<span data-ttu-id="16cbe-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="16cbe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="16cbe-104">Spécifie le fonctionnement de la méthode [MoveRecord](record-object-ado.md) de l'objet [Record](moverecord-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="16cbe-104">Specifies the behavior of the [Record](record-object-ado.md) object [MoveRecord](moverecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16cbe-105">Constant</span><span class="sxs-lookup"><span data-stu-id="16cbe-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="16cbe-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="16cbe-106">Value</span></span></p></th>
<th><p><span data-ttu-id="16cbe-107">Description</span><span class="sxs-lookup"><span data-stu-id="16cbe-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16cbe-108"><strong>adMoveUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="16cbe-108"><strong>adMoveUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="16cbe-109">-1</span><span class="sxs-lookup"><span data-stu-id="16cbe-109">-1</span></span></p></td>
<td><p><span data-ttu-id="16cbe-p101">Par défaut. Effectue l'opération de déplacement par défaut : l'opération échoue si le fichier ou répertoire de destination existe déjà ; elle met alors à jour les liens hypertexte.</span><span class="sxs-lookup"><span data-stu-id="16cbe-p101">Default. Performs the default move operation: The operation fails if the destination file or directory already exists, and the operation updates hypertext links.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16cbe-112"><strong>adMoveOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="16cbe-112"><strong>adMoveOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="16cbe-113">1</span><span class="sxs-lookup"><span data-stu-id="16cbe-113">1</span></span></p></td>
<td><p><span data-ttu-id="16cbe-114">Remplace le fichier ou répertoire de destination, même s'il existe déjà.</span><span class="sxs-lookup"><span data-stu-id="16cbe-114">Overwrites the destination file or directory, even if it already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16cbe-115"><strong>adMoveDontUpdateLinks</strong></span><span class="sxs-lookup"><span data-stu-id="16cbe-115"><strong>adMoveDontUpdateLinks</strong></span></span></p></td>
<td><p><span data-ttu-id="16cbe-116">2</span><span class="sxs-lookup"><span data-stu-id="16cbe-116">2</span></span></p></td>
<td><p><span data-ttu-id="16cbe-p102">Modifie le fonctionnement par défaut de la méthode <strong>MoveRecord</strong> en ne mettant pas à jour les liens hypertexte du <strong>Record</strong> source. Le fonctionnement par défaut dépend des capacités du fournisseur. L'opération Move met à jour les liens si le fournisseur en est capable. Si le fournisseur ne peut résoudre les liens ou si cette valeur n'est pas spécifiée, le déplacement réussit même si les liens n'ont pas été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="16cbe-p102">Modifies the default behavior of <strong>MoveRecord</strong> method by not updating the hypertext links of the source <strong>Record</strong>. The default behavior depends on the capabilities of the provider. Move operation updates links if the provider is capable. If the provider cannot fix links or if this value is not specified, then the move succeeds even when links have not been fixed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16cbe-121"><strong>adMoveAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="16cbe-121"><strong>adMoveAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="16cbe-122">4</span><span class="sxs-lookup"><span data-stu-id="16cbe-122">4</span></span></p></td>
<td><p><span data-ttu-id="16cbe-p103">Demande au fournisseur de simuler le déplacement (à l'aide d'opérations de téléchargement, de chargement et de suppression). Si la tentative de déplacement du <strong>Record</strong> échoue parce que l'URL de destination se trouve sur un autre serveur ou si elle est servie par un autre fournisseur que la source des données, il peut en résulter une latence accrue ou une perte de données, en raison des caractéristiques différentes des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="16cbe-p103">Requests that the provider attempt to simulate the move (using download, upload, and delete operations). If the attempt to move the <strong>Record</strong> fails because the destination URL is on a different server or serviced by a different provider than the source, this may cause increased latency or data loss, due to different provider capabilities when moving resources between providers.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16cbe-125">**Équivalent ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="16cbe-125">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="16cbe-126">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="16cbe-126">These constants do not have ADO/WFC equivalents.</span></span>

