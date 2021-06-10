---
title: Field2.ValidationText, propriété (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4d58cb6bd32bd46b0a6bcec40ff68cdc52eebc31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292621"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="53eca-102">Field2.ValidationText, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="53eca-102">Field2.ValidationText property (DAO)</span></span>


<span data-ttu-id="53eca-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53eca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53eca-p101">Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet **Field2** ne respecte par la règle de validation spécifiée par le paramètre de propriété **ValidationRule** (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="53eca-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="53eca-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53eca-106">Syntax</span></span>

<span data-ttu-id="53eca-107">*.* ValidationText</span><span class="sxs-lookup"><span data-stu-id="53eca-107">*expression* .ValidationText</span></span>

<span data-ttu-id="53eca-108">*expression* une variable qui représente une **champ2** objet.</span><span class="sxs-lookup"><span data-stu-id="53eca-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="53eca-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="53eca-109">Remarks</span></span>

<span data-ttu-id="53eca-p102">Le paramètre ou la valeur de retour est une **String** qui spécifie le texte affiché si un utilisateur tente d'entrer une valeur non valide pour un champ. Pour un objet pas encore ajouté à une collection, cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="53eca-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="53eca-112">Pour un objet **Field2**, l'utilisation de la propriété **ValidationText** dépend de l'objet qui contient la collection **[Fields](fields-collection-dao.md)** à laquelle l'objet **Field2** est ajouté, comme illustré dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="53eca-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53eca-113">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="53eca-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="53eca-114">Utilisation</span><span class="sxs-lookup"><span data-stu-id="53eca-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53eca-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="53eca-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="53eca-116">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="53eca-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53eca-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="53eca-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="53eca-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53eca-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53eca-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="53eca-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="53eca-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="53eca-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53eca-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="53eca-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="53eca-122">Non reconnu</span><span class="sxs-lookup"><span data-stu-id="53eca-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53eca-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="53eca-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="53eca-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="53eca-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

