---
title: 'Chapitre 9 : Mise en forme de données'
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 988766f71fd57505693683d54a15b13409ae6960
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875874"
---
# <a name="chapter-9-data-shaping"></a><span data-ttu-id="06092-102">Chapitre 9 : Mise en forme de données</span><span class="sxs-lookup"><span data-stu-id="06092-102">Chapter 9: Data Shaping</span></span>


<span data-ttu-id="06092-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06092-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06092-104">*Mise en forme des données* fournit un moyen pour interroger une source de données et de renvoyer un [objet Recordset](recordset-object-ado.md) qui représente une relation parent-enfant entre deux ou plusieurs entités logiques (une hiérarchie).</span><span class="sxs-lookup"><span data-stu-id="06092-104">*Data shaping* provides a way to query a data source and return a [Recordset](recordset-object-ado.md) that represents a parent-child relationship between two or more logical entities (a hierarchy).</span></span> <span data-ttu-id="06092-105">Des clients et des commandes constituent un exemple de relation hiérarchique classique.</span><span class="sxs-lookup"><span data-stu-id="06092-105">A classic example of a hierarchical relationship is customers and orders.</span></span> <span data-ttu-id="06092-106">Ainsi, à chaque client d'une base de données correspond zéro ou plusieurs commandes.</span><span class="sxs-lookup"><span data-stu-id="06092-106">For every customer in a database, there can be zero or more orders.</span></span> <span data-ttu-id="06092-107">Bien que les requêtes SQL normales fournissent un moyen d'extraire les données à l'aide de la syntaxe JOIN, celles-ci peuvent s'avérer inefficaces et difficiles à manipuler, car des données parentes redondantes sont répétées dans chaque enregistrement renvoyé pour une relation parent-enfant donnée.</span><span class="sxs-lookup"><span data-stu-id="06092-107">Regular SQL provides a means of retrieving the data using JOIN syntax, but this can be inefficient and unwieldy because redundant parent data is repeated in each record returned for a given parent-child relationship.</span></span> <span data-ttu-id="06092-108">La mise en forme des données peut associer un seul enregistrement parent de l'objet **Recordset** parent à plusieurs enregistrements enfants de l'objet **Recordset** enfant, ce qui évite la redondance inhérente à une opération de jointure.</span><span class="sxs-lookup"><span data-stu-id="06092-108">Data shaping can relate a single parent record in the parent **Recordset** to multiple child records in the child **Recordset**, avoiding the redundancy of a JOIN.</span></span> <span data-ttu-id="06092-109">Nombreux sont ceux qui trouvent le modèle de programmation de plusieurs objets **Recordset** parent-enfants plus naturel et plus facile à manipuler que le modèle JOIN reposant sur un seul objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="06092-109">Most people find the parent-child multiple **Recordset** programming model more natural and easier to work with than the single **Recordset** JOIN model.</span></span>

<span data-ttu-id="06092-p102">La syntaxe de mise en forme des données fournit aussi d'autres fonctionnalités. Elle permet notamment aux développeurs de créer de nouveaux objets **Recordset** sans source de données sous-jacente à l'aide du mot-clé NEW. Ce mot-clé permet de décrire les champs des objets **Recordset** parents et enfants. Le nouvel objet **Recordset** peut être rempli avec des données et stocké de façon persistante. La syntaxe de mise en forme permet également aux développeurs d'effectuer divers calculs ou agrégations (par exemple, SUM, AVG et MAX) sur les champs enfants ainsi que de créer un objet **Recordset** parent à partir d'un objet **Recordset** enfant en groupant les enregistrements dans l'enregistrement enfant et en plaçant une ligne dans l'enregistrement parent pour chaque groupe dans l'enfant.</span><span class="sxs-lookup"><span data-stu-id="06092-p102">The data shaping syntax also provides other capabilities. Developers can create new **Recordset** objects without an underlying data source by using the NEW keyword to describe the fields of the parent and child **Recordsets**. The new **Recordset** object can be populated with data and persistently stored. Developers can also perform various calculations or aggregations (for example, SUM, AVG, and MAX) on child fields. Data shaping can also create a parent **Recordset** from a child **Recordset** by grouping records in the child and placing one row in the parent for each group in the child.</span></span>

<span data-ttu-id="06092-115">Consultez les rubriques suivantes pour en savoir plus sur la mise en forme des données :</span><span class="sxs-lookup"><span data-stu-id="06092-115">See the following topics to learn more about data shaping:</span></span>

- [<span data-ttu-id="06092-116">Fournisseurs requis pour la mise en forme des données</span><span class="sxs-lookup"><span data-stu-id="06092-116">Required Providers for Data Shaping</span></span>](required-providers-for-data-shaping.md)

- [<span data-ttu-id="06092-117">Forme Compute, Clause</span><span class="sxs-lookup"><span data-stu-id="06092-117">Shape Compute Clause</span></span>](shape-compute-clause.md)

- [<span data-ttu-id="06092-118">Création de jeux d'enregistrements hiérarchiques</span><span class="sxs-lookup"><span data-stu-id="06092-118">Fabricating Hierarchical Recordsets</span></span>](fabricating-hierarchical-recordsets.md)

- [<span data-ttu-id="06092-119">Accès aux lignes d'un jeu d'enregistrements hiérarchique</span><span class="sxs-lookup"><span data-stu-id="06092-119">Accessing Rows in a Hierarchical Recordset</span></span>](accessing-rows-in-a-hierarchical-recordset.md)

- [<span data-ttu-id="06092-120">Grammaire de mise en forme formelle</span><span class="sxs-lookup"><span data-stu-id="06092-120">Formal Shape Grammar</span></span>](formal-shape-grammar.md)

- [<span data-ttu-id="06092-121">Visual Basic pour Applications functions</span><span class="sxs-lookup"><span data-stu-id="06092-121">Visual Basic for Applications functions</span></span>](visual-basic-for-applications-functions.md)

- [<span data-ttu-id="06092-122">Shape Append Clause (ADO)</span><span class="sxs-lookup"><span data-stu-id="06092-122">Shape Append Clause (ADO)</span></span>](shape-append-clause.md)

- [<span data-ttu-id="06092-123">Data Shaping (ADO)</span><span class="sxs-lookup"><span data-stu-id="06092-123">Data Shaping (ADO)</span></span>](data-shaping.md)

- [<span data-ttu-id="06092-124">Shape Commands in General (ADO)</span><span class="sxs-lookup"><span data-stu-id="06092-124">Shape Commands in General (ADO)</span></span>](shape-commands-in-general.md)

