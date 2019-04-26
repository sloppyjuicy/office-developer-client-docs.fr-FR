---
title: CREATE VIEW, instruction (Microsoft Access SQL)
TOCTitle: CREATE VIEW statement (Microsoft Access SQL)
ms:assetid: ecaabd75-3081-fd35-830d-5a59b0a51922
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836312(v=office.15)
ms:contentKeyID: 48548519
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 73fac5ff9dd1f5cf277b8cb241044af23609b764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295365"
---
# <a name="create-view-statement-microsoft-access-sql"></a><span data-ttu-id="fc8c0-102">CREATE VIEW, instruction (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="fc8c0-102">CREATE VIEW Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="fc8c0-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc8c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc8c0-104">Crée un affichage.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-104">Creates a new view.</span></span>

> [!NOTE]
> <span data-ttu-id="fc8c0-105">Le moteur de base de données Microsoft Access ne prend pas en charge l’utilisation de CRÉER UN AFFICHAGE, ni d’aucune des instructions DDL, avec des bases de données d’un moteur de base de données autre que Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-105">The Microsoft Access database engine does not support the use of CREATE VIEW, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8c0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc8c0-106">Syntax</span></span>

<span data-ttu-id="fc8c0-107">CREATE VIEW *view* \[(*field1*\[, *field2*\[, …\]\])\] AS *selectstatement*</span><span class="sxs-lookup"><span data-stu-id="fc8c0-107">CREATE VIEW *view [(field1* \[[, *field2*[, …]])] AS *selectstatement*</span></span>

<span data-ttu-id="fc8c0-108">L’instruction CRÉER UN AFFICHAGE est composée des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="fc8c0-108">The CREATE VIEW statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc8c0-109">Quitter</span><span class="sxs-lookup"><span data-stu-id="fc8c0-109">Part</span></span></p></th>
<th><p><span data-ttu-id="fc8c0-110">Description</span><span class="sxs-lookup"><span data-stu-id="fc8c0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc8c0-111"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="fc8c0-111"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="fc8c0-112">Nom de l’affichage à créer.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-112">The name of the view to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc8c0-113"><em>champ1</em>, <em>champ2</em></span><span class="sxs-lookup"><span data-stu-id="fc8c0-113"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="fc8c0-114">Nom du ou des champs pour les champs correspondants spécifiés dans <em>instructionselect</em>.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-114">The name of field or fields for the corresponding fields specified in <em>selectstatement</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc8c0-115"><em>instructionselect</em></span><span class="sxs-lookup"><span data-stu-id="fc8c0-115">AS <em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="fc8c0-116">Instruction SELECT SQL.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-116">A SQL SELECT statement.</span></span> <span data-ttu-id="fc8c0-117">Pour plus d’informations, voir <a href="select-statement-microsoft-access-sql.md">SELECT, instruction</a>.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-117">For more information, see <a href="select-statement-microsoft-access-sql.md">SELECT Statement</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fc8c0-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc8c0-118">Remarks</span></span>

<span data-ttu-id="fc8c0-119">L’instruction SELECT qui définit l’affichage ne peut pas être une instruction [SELECT INTO](select-into-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="fc8c0-119">The SELECT statement that defines the view cannot be a [SELECT INTO](select-into-statement-microsoft-access-sql.md) statement.</span></span>

<span data-ttu-id="fc8c0-120">L’instruction SELECT qui définit l’affichage ne peut pas contenir de paramètres.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-120">The SELECT statement that defines the view cannot contain any parameters.</span></span>

<span data-ttu-id="fc8c0-121">Le nom de l’affichage ne peut pas être identique au nom d’une table existante.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-121">The name of the view cannot be the same as the name of an existing table.</span></span>

<span data-ttu-id="fc8c0-122">Si la requête définie par l'instruction SELECT est modifiable, l'affichage l'est également.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-122">If the query defined by the SELECT statement is updatable, then the view is also updatable.</span></span> <span data-ttu-id="fc8c0-123">Sinon, l’affichage est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-123">Otherwise, the view is read-only.</span></span>

<span data-ttu-id="fc8c0-124">Si deux des champs de la requête définis par l’instruction SELECT ont le même nom, la définition de l’affichage doit comporter une liste de champs spécifiant des noms uniques pour chacun des champs de la requête.</span><span class="sxs-lookup"><span data-stu-id="fc8c0-124">If any two fields in the query defined by the SELECT statement have the same name, the view definition must include a field list specifying unique names for each of the fields in the query.</span></span>

