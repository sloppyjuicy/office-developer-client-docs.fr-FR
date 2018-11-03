---
title: Propriété Field.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3244c4e41761095378e3be3ad928effc6444f842
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930405"
---
# <a name="fieldvalidationtext-property-dao"></a><span data-ttu-id="4e1f1-102">Propriété Field.ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="4e1f1-102">Field.ValidationText property (DAO)</span></span>


<span data-ttu-id="4e1f1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e1f1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e1f1-p101">Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet **Field** n'est pas conforme à la règle de validation spécifiée par la valeur de la propriété **ValidationRule** (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="4e1f1-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1f1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e1f1-106">Syntax</span></span>

<span data-ttu-id="4e1f1-107">*expression* . ValidationText (MessageSiErreur)</span><span class="sxs-lookup"><span data-stu-id="4e1f1-107">*expression* .ValidationText</span></span>

<span data-ttu-id="4e1f1-108">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="4e1f1-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e1f1-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e1f1-109">Remarks</span></span>

<span data-ttu-id="4e1f1-p102">Le paramètre ou la valeur de retour est une chaîne (type de données **String**) qui spécifie le texte affiché lorsqu'un utilisateur tente d'entrer une valeur non valide dans un champ. Cette propriété est en lecture/écriture pour les objets non encore ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="4e1f1-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="4e1f1-112">Pour un objet **Field**, l'utilisation de la propriété **ValidationText** dépend de l'objet contenant la collection **[Fields](fields-collection-dao.md)** à laquelle est ajouté l'objet **Field**, comme le montre le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4e1f1-112">For a **Field** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e1f1-113">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="4e1f1-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="4e1f1-114">Utilisation</span><span class="sxs-lookup"><span data-stu-id="4e1f1-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e1f1-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="4e1f1-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4e1f1-116">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e1f1-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1f1-117"><strong>Objet QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="4e1f1-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4e1f1-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e1f1-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1f1-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="4e1f1-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="4e1f1-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4e1f1-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e1f1-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="4e1f1-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="4e1f1-122">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e1f1-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e1f1-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="4e1f1-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4e1f1-124">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="4e1f1-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

