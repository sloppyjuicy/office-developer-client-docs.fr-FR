---
title: Propriété Field.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47bd400469bc17ac2b57bb249198f7609d7d0801
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721107"
---
# <a name="fieldvalidationtext-property-dao"></a><span data-ttu-id="ca64e-102">Propriété Field.ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="ca64e-102">Field.ValidationText property (DAO)</span></span>


<span data-ttu-id="ca64e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca64e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ca64e-p101">Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet **Field** n'est pas conforme à la règle de validation spécifiée par la valeur de la propriété **ValidationRule** (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="ca64e-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca64e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca64e-106">Syntax</span></span>

<span data-ttu-id="ca64e-107">*expression* . ValidationText (MessageSiErreur)</span><span class="sxs-lookup"><span data-stu-id="ca64e-107">*expression* .ValidationText</span></span>

<span data-ttu-id="ca64e-108">*expression* Variable qui représente un objet **Field** .</span><span class="sxs-lookup"><span data-stu-id="ca64e-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca64e-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca64e-109">Remarks</span></span>

<span data-ttu-id="ca64e-p102">Le paramètre ou la valeur de retour est une chaîne (type de données **String**) qui spécifie le texte affiché lorsqu'un utilisateur tente d'entrer une valeur non valide dans un champ. Cette propriété est en lecture/écriture pour les objets non encore ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="ca64e-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="ca64e-112">Pour un objet **Field**, l'utilisation de la propriété **ValidationText** dépend de l'objet contenant la collection **[Fields](fields-collection-dao.md)** à laquelle est ajouté l'objet **Field**, comme le montre le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ca64e-112">For a **Field** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca64e-113">Objet ajouté à</span><span class="sxs-lookup"><span data-stu-id="ca64e-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="ca64e-114">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ca64e-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca64e-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="ca64e-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="ca64e-116">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca64e-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca64e-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="ca64e-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="ca64e-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca64e-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca64e-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="ca64e-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="ca64e-120">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ca64e-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca64e-121"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="ca64e-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="ca64e-122">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca64e-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca64e-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="ca64e-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="ca64e-124">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="ca64e-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

