---
title: Généralités sur les commandes de mise en forme (SHAPE)
TOCTitle: Shape Commands in General
ms:assetid: ad555aa7-bc64-b495-a98d-e927061a5809
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249814(v=office.15)
ms:contentKeyID: 48547039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 33570bec65de4ff88667ad90b591c4f288c86d96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470946"
---
# <a name="shape-commands-in-general"></a><span data-ttu-id="6976d-102">Généralités sur les commandes de mise en forme (SHAPE)</span><span class="sxs-lookup"><span data-stu-id="6976d-102">Shape Commands in General</span></span>


<span data-ttu-id="6976d-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6976d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6976d-104">La mise en forme des données définit les colonnes d'un objet **Recordset** mis en forme, la relation entre les entités représentées par les colonnes et la façon dont un objet **Recordset** est rempli avec des données.</span><span class="sxs-lookup"><span data-stu-id="6976d-104">Data shaping defines the columns of a shaped **Recordset**, the relationships between the entities represented by the columns, and the manner in which the **Recordset** is populated with data.</span></span>

<span data-ttu-id="6976d-105">Un objet **Recordset** mis en forme peut se composer des types de colonnes suivants.</span><span class="sxs-lookup"><span data-stu-id="6976d-105">A shaped **Recordset** may consist of the following types of columns.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6976d-106">Type de colonne</span><span class="sxs-lookup"><span data-stu-id="6976d-106">Column type</span></span></p></th>
<th><p><span data-ttu-id="6976d-107">Description</span><span class="sxs-lookup"><span data-stu-id="6976d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6976d-108">data</span><span class="sxs-lookup"><span data-stu-id="6976d-108">data</span></span></p></td>
<td><p><span data-ttu-id="6976d-109">Champs d’un objet <strong>Recordset</strong> retournés par une commande de requête à un fournisseur de données, une table ou un objet <strong>Recordset</strong> préalablement mis en forme.</span><span class="sxs-lookup"><span data-stu-id="6976d-109">Fields from a <strong>Recordset</strong> returned by a query command to a data provider, table, or previously shaped <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6976d-110">chapitre</span><span class="sxs-lookup"><span data-stu-id="6976d-110">chapter</span></span></p></td>
<td><p><span data-ttu-id="6976d-p101">Référence à un autre objet <strong>Recordset</strong>, appelée <em>chapitre</em>. Les colonnes de chapitre permettent de définir une relation <em>parent-enfant</em> dans laquelle le <em>parent</em> est l'objet <strong>Recordset</strong> contenant la colonne de chapitre et l'<em>enfant</em> est l'objet <strong>Recordset</strong> représenté par le chapitre.</span><span class="sxs-lookup"><span data-stu-id="6976d-p101">A reference to another <strong>Recordset</strong>, called a <em>chapter</em>. Chapter columns make it possible to define a <em>parent-child</em> relationship where the <em>parent</em> is the <strong>Recordset</strong> containing the chapter column and the <em>child</em> is the <strong>Recordset</strong> represented by the chapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6976d-113">agrégat</span><span class="sxs-lookup"><span data-stu-id="6976d-113">aggregate</span></span></p></td>
<td><p><span data-ttu-id="6976d-p102">La valeur de la colonne est obtenue par l’exécution d’une <em>fonction d’agrégation</em> sur toutes les lignes ou une colonne de toutes les lignes d’un objet <strong>Recordset</strong>.(Consultez la section relative aux fonctions d’agrégation dans la rubrique <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Fonctions d’agrégation, fonction CALC et mot clé NEW</a>.)</span><span class="sxs-lookup"><span data-stu-id="6976d-p102">The value of the column is derived by executing an <em>aggregate function</em> on all the rows or a column of all the rows of a child <strong>Recordset</strong>. (See Aggregate Functions in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6976d-116">expression calculée</span><span class="sxs-lookup"><span data-stu-id="6976d-116">calculated expression</span></span></p></td>
<td><p><span data-ttu-id="6976d-p103">La valeur de la colonne est obtenue par le calcul d’une expression Visual Basic pour Applications sur les colonnes d’une même ligne de l’objet <strong>Recordset</strong>.  L’expression est l’argument de la fonction CALC. (Consultez la section Expression calculée dans les rubriques<a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Fonctions d’agrégation, fonction CALC et mot clé NEW</a> et <a href="visual-basic-for-applications-functions.md">Fonctions Visual Basic pour Applications</a>.)</span><span class="sxs-lookup"><span data-stu-id="6976d-p103">The value of the column is derived by calculating a Visual Basic for Applications expression on columns in the same row of the <strong>Recordset</strong>. The expression is the argument to the CALC function. (See Calculated Expression in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a> and in <a href="visual-basic-for-applications-functions.md">Visual Basic for Applications Functions</a>.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6976d-120">nouveau</span><span class="sxs-lookup"><span data-stu-id="6976d-120">new</span></span></p></td>
<td><p><span data-ttu-id="6976d-p104">Champs créés et vides qui peuvent être ultérieurement remplis avec des données. La colonne est définie avec le mot-clé NEW. (Voir la section consacrée au mot-clé NEW dans la rubrique <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Fonctions d’agrégation, fonction CALC et mot clé NEW</a>.)</span><span class="sxs-lookup"><span data-stu-id="6976d-p104">Empty, fabricated fields, which may be populated with data at a later time. The column is defined with the NEW keyword. (See NEW keyword in the following topic, <a href="aggregate-functions-the-calc-function-and-the-new-keyword.md">Aggregate Functions, the CALC Function, and the NEW Keyword</a>.)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6976d-p105">Une commande SHAPE peut contenir une clause qui spécifie une commande de requête destinée à un fournisseur de données sous-jacent qui retournera un objet **Recordset**. La syntaxe de la requête dépend des exigences du fournisseur de données sous-jacent. Elle est en général écrite en langage SQL, même si ADO ne requiert pas de langage particulier.</span><span class="sxs-lookup"><span data-stu-id="6976d-p105">A shape command may contain a clause specifying a query command to an underlying data provider that will return a **Recordset** object. The query's syntax depends on the requirements of the underlying data provider. This will usually be Structured Query Language (SQL), although ADO does not require the use of any particular query language.</span></span>

<span data-ttu-id="6976d-p106">Vous pouvez utiliser une clause JOIN SQL pour établir une relation entre deux tables ; cependant, sachez qu'un objet **Recordset** hiérarchique peut représenter les informations de manière plus efficace. Chaque ligne d'un objet **Recordset** créé par une clause JOIN reproduit les informations de l'une des tables de façon redondante. En revanche, un objet **Recordset** hiérarchique ne comporte qu'un objet **Recordset** parent pour chacun des différents objets **Recordset** enfant.</span><span class="sxs-lookup"><span data-stu-id="6976d-p106">You could use a SQL JOIN clause to relate two tables; however, a hierarchical **Recordset** may represent the information more efficiently. Each row of a **Recordset** created by a JOIN repeats information redundantly from one of the tables. A hierarchical **Recordset** has only one parent **Recordset** for each of multiple child **Recordset** objects.</span></span>

<span data-ttu-id="6976d-130">Les commandes SHAPE peuvent être émises par des objets **Recordset** ou en définissant la propriété [CommandText](commandtext-property-ado.md) de l'objet [Command](command-object-ado.md), puis en appelant la méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="6976d-130">Shape commands can be issued by **Recordset** objects or by setting the [CommandText](commandtext-property-ado.md) property of the [Command](command-object-ado.md) object and then calling the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>

<span data-ttu-id="6976d-131">Elles peuvent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="6976d-131">Shape commands can be nested.</span></span> <span data-ttu-id="6976d-132">Autrement dit, le *parent-command* ou *child-command* lui-même peut-être autre commande shape.</span><span class="sxs-lookup"><span data-stu-id="6976d-132">That is, the *parent-command* or *child-command* may itself be another shape command.</span></span>

<span data-ttu-id="6976d-133">Le fournisseur de mise en forme retourne toujours un curseur client, même lorsque l'utilisateur spécifie **adUseServer** comme emplacement de curseur.</span><span class="sxs-lookup"><span data-stu-id="6976d-133">The shape provider always returns a client cursor, even when the user specifies a cursor location of **adUseServer**.</span></span>

<span data-ttu-id="6976d-134">Pour plus d'informations sur la navigation au sein d'un objet **Recordset** hiérarchique, consultez [Accès aux lignes d'un jeu d'enregistrements hiérarchique](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="6976d-134">For information about navigating a hierarchical **Recordset**, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="6976d-135">Pour obtenir des informations détaillées sur la syntaxe des commandes SHAPE, consultez [Grammaire de mise en forme formelle](formal-shape-grammar.md).</span><span class="sxs-lookup"><span data-stu-id="6976d-135">For precise information about syntactically correct shape commands, see [Formal Shape Grammar](formal-shape-grammar.md).</span></span>

