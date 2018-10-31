---
title: Instruction CREATE VIEW (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f1d13cef4551975dc316b2fbedf2388028956fb3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862904"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="ffe8c-102">Instruction CREATE VIEW (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="ffe8c-102">CREATE VIEW statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="ffe8c-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffe8c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ffe8c-104">Crée un nouvel affichage.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-104">Creates a new view.</span></span>

> [!NOTE]
> <span data-ttu-id="ffe8c-105">[!REMARQUE] Le moteur de base de données Microsoft Access ne prend pas en charge l'instruction CREATE VIEW, ni les instructions DDL, avec les bases de données autres que Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe8c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffe8c-106">Syntax</span></span>

<span data-ttu-id="ffe8c-107">CREATE VIEW *affichage* \[(*champ1*\[, *champ2*\[,... \] \])\] AS *instructionselect*</span><span class="sxs-lookup"><span data-stu-id="ffe8c-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span></span>

<span data-ttu-id="ffe8c-108">L'instruction CREATE VIEW est composée des arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ffe8c-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ffe8c-109">Argument</span><span class="sxs-lookup"><span data-stu-id="ffe8c-109">Part</span></span></p></th>
<th><p><span data-ttu-id="ffe8c-110">Description</span><span class="sxs-lookup"><span data-stu-id="ffe8c-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ffe8c-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="ffe8c-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="ffe8c-112">Nom de l'affichage à créer.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ffe8c-113"><em>champ1</em>, <em>champ2</em></span><span class="sxs-lookup"><span data-stu-id="ffe8c-113"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="ffe8c-114">Nom des champs correspondants spécifiés dans <em>instuctionselect</em>.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ffe8c-115"><em>instructionselect</em></span><span class="sxs-lookup"><span data-stu-id="ffe8c-115"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="ffe8c-116">Instruction SELECT SQL.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-116">A SQL SELECT statement.</span></span> <span data-ttu-id="ffe8c-117">Pour plus d’informations, voir <a href="select-statement-microsoft-access-sql.md">l’instruction SELECT</a>.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ffe8c-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ffe8c-118">Remarks</span></span>

<span data-ttu-id="ffe8c-119">L'instruction SELECT qui définit l'affichage ne peut pas être une instruction [SELECT INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="ffe8c-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="ffe8c-120">Cette instruction ne peut pas non plus contenir de paramètres.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="ffe8c-121">Le nom de l'affichage ne peut pas être le même que le nom d'une table existante.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="ffe8c-122">Si la requête définie par l’instruction SELECT est modifiable, l’affichage est également être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-122">If the query defined by the SELECT statement is updatable, the view is also updatable.</span></span> <span data-ttu-id="ffe8c-123">Sinon, l'affichage est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-123">Otherwise, the view is read-only.</span></span>

<span data-ttu-id="ffe8c-124">Si deux champs dans la requête définie par l'instruction SELECT ont le même nom, la définition de l'affichage doit inclure une liste de noms uniques pour les champs dans la requête.</span><span class="sxs-lookup"><span data-stu-id="ffe8c-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

