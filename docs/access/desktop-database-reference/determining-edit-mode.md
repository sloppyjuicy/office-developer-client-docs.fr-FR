---
title: Détermination du mode de modification
TOCTitle: Determining Edit Mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: facad27e4579a28f45d88bfd4e440e420e70d913
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867936"
---
# <a name="determining-edit-mode"></a><span data-ttu-id="48b0c-102">Détermination du mode de modification</span><span class="sxs-lookup"><span data-stu-id="48b0c-102">Determining Edit Mode</span></span>


<span data-ttu-id="48b0c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48b0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48b0c-p101">ADO gère une mémoire tampon de modification associée à l'enregistrement actif. La propriété **EditMode** indique si cette mémoire tampon a été modifiée ou si un nouvel enregistrement a été créé. Utilisez **EditMode** pour déterminer l'état de modification de l'enregistrement actif. Vous pouvez vérifier s'il existe des modifications en attente en cas d'interruption d'un processus de modification et déterminer si vous avez besoin d'utiliser la méthode **Update** ou **CancelUpdate**.</span><span class="sxs-lookup"><span data-stu-id="48b0c-p101">ADO maintains an editing buffer associated with the current record. The **EditMode** property indicates whether changes have been made to this buffer or whether a new record has been created. Use **EditMode** to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the **Update** or **CancelUpdate** method.</span></span>

<span data-ttu-id="48b0c-108">**EditMode** retourne une des constantes **EditModeEnum**, telles qu'elles sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="48b0c-108">**EditMode** returns one of the **EditModeEnum** constants, which are listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="48b0c-109">Constant</span><span class="sxs-lookup"><span data-stu-id="48b0c-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="48b0c-110">Description</span><span class="sxs-lookup"><span data-stu-id="48b0c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48b0c-111"><strong>adEditNone</strong></span><span class="sxs-lookup"><span data-stu-id="48b0c-111"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="48b0c-112">Indique qu'aucune opération d'édition n'est en cours.</span><span class="sxs-lookup"><span data-stu-id="48b0c-112">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48b0c-113"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="48b0c-113"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="48b0c-114">Indique que les données de l'enregistrement en cours ont été modifiées, mais pas enregistrées.</span><span class="sxs-lookup"><span data-stu-id="48b0c-114">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48b0c-115"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="48b0c-115"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="48b0c-116">Indique que la méthode <strong>AddNew</strong> a été appelée et que l'enregistrement actif dans le tampon de copie est un nouvel enregistrement qui n'a pas été enregistré dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="48b0c-116">Indicates that the <strong>AddNew</strong> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48b0c-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="48b0c-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="48b0c-118">Indique que l'enregistrement en cours a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="48b0c-118">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="48b0c-p102">**EditMode** peut retourner une valeur valide seulement s'il existe un enregistrement actif. **EditMode** retourne une erreur si la propriété **BOF** ou **EOF** a la valeur **True** ou si l'enregistrement actif a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="48b0c-p102">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if **BOF** or **EOF** is **True** or if the current record has been deleted.</span></span>

