---
title: Définition d'un curseur  (Référence de base de données du bureau access)
TOCTitle: What is a Cursor?
ms:assetid: cc70d941-05e0-9b14-1c5d-6b1a5802f546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250013(v=office.15)
ms:contentKeyID: 48547738
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6dc2e38c7459fea46c33373447276d8643b4b0de
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887375"
---
# <a name="what-is-a-cursor"></a><span data-ttu-id="a3732-103">Qu’est-ce qu’un curseur ?</span><span class="sxs-lookup"><span data-stu-id="a3732-103">What is a Cursor?</span></span>


<span data-ttu-id="a3732-104">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3732-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3732-p102">Les opérations effectuées dans une base de données relationnelle s'appliquent à l'ensemble d'un jeu de lignes. Le jeu de lignes renvoyé par une instruction SELECT comprend toutes les lignes qui répondent aux conditions de la clause WHERE de l'instruction. Ce jeu de lignes complet, retourné par l'instruction, est appelé « jeu de résultats ». Dans certaines applications, plus particulièrement les applications interactives et en ligne, le traitement global du jeu de résultats présente parfois des difficultés. Ces applications requièrent un mécanisme spécifique leur permettant de traiter une ligne ou un petit ensemble de lignes à la fois. Un curseur constitue une extension au jeux de résultats qui fournit ce mécanisme.</span><span class="sxs-lookup"><span data-stu-id="a3732-p102">Operations in a relational database act on a complete set of rows. The set of rows returned by a SELECT statement consists of all the rows that satisfy the conditions in the WHERE clause of the statement. This complete set of rows returned by the statement is known as the result set. Applications, especially those that are interactive and online, cannot always work effectively with the entire result set as a unit. These applications need a mechanism to work with one row or a small block of rows at a time. Cursors are an extension to result sets that provide that mechanism.</span></span>

<span data-ttu-id="a3732-p103">Un curseur est implémenté par une bibliothèque de curseurs. Une bibliothèque de curseurs est un logiciel implémenté la plupart du temps au sein d'un système de base de données ou d'une API d'accès aux données, qui permet la gestion des attributs de données renvoyées par une source de données (jeu de résultats). Ces attributs concernent la gestion de l'accès simultané, la position dans le jeu de résultats, le nombre de lignes renvoyées et la possibilité de défilement avant ou arrière dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="a3732-p103">A cursor is implemented by a cursor library. A cursor library is software, often implemented as a part of a database system or a data access API, that is used to manage attributes of data returned from a data source (a result set). These attributes include concurrency management, position in the result set, number of rows returned, and whether or not you can move forward and/or backward through the result set (scrollability).</span></span>

<span data-ttu-id="a3732-p104">Un curseur peut effectuer un suivi de la position dans le jeu de résultats, et permet d'effectuer un grand nombre d'opérations, ligne par ligne, dans un jeu de résultats, sans devoir nécessairement revenir à la table initiale. En d'autres termes, les curseurs sont conçus pour renvoyer un jeu de résultats basé sur des tables de bases de données. Le curseur est ainsi nommé car il indique la position active dans le jeu de résultats, à l'instar du curseur de l'écran de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a3732-p104">A cursor keeps track of the position in the result set, and allows you to perform multiple operations row by row against a result set, with or without returning to the original table. In other words, cursors conceptually return a result set based on tables within the databases. The cursor is so named because it indicates the current position in the result set, just as the cursor on a computer screen indicates current position.</span></span>

<span data-ttu-id="a3732-117">Il est important de maîtriser le concept du curseur avant de passer aux spécificités de son utilisation dans ADO.</span><span class="sxs-lookup"><span data-stu-id="a3732-117">It is important to become familiar with the concept of cursors before moving on to learn the specifics of their usage in ADO.</span></span>

<span data-ttu-id="a3732-118">Les curseurs permettent d'effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="a3732-118">Using cursors, you can:</span></span>

  - <span data-ttu-id="a3732-119">Spécifier des positions sur des lignes spécifiques d'un jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="a3732-119">Specify positioning at specific rows in the result set.</span></span>

  - <span data-ttu-id="a3732-120">Extraire une ligne ou un bloc de lignes en fonction de la position active dans le jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="a3732-120">Retrieve one row or a block of rows based on the current result set position.</span></span>

  - <span data-ttu-id="a3732-121">Modifier les données des lignes au niveau de la position active dans le jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="a3732-121">Modify data in the rows at the current position in the result set.</span></span>

  - <span data-ttu-id="a3732-122">Définir plusieurs niveaux de sensibilité des modifications apportées aux données par d'autres utilisateurs</span><span class="sxs-lookup"><span data-stu-id="a3732-122">Define different levels of sensitivity to data changes made by other users.</span></span>

<span data-ttu-id="a3732-p105">Imaginons par exemple une application qui présente à un acheteur potentiel une liste de plusieurs produits. L'acheteur peut faire défiler la liste pour accéder aux informations et aux prix des produits, puis sélectionner un produit à acheter. Un défilement et une sélection supplémentaires s'appliquent au reste de la liste. Du point de vue de l'acheteur, les produits s'affichent un par un, mais l'application utilise un curseur de défilement vertical pour parcourir le jeu de résultats en amont et en aval.</span><span class="sxs-lookup"><span data-stu-id="a3732-p105">For example, consider an application that displays a list of available products to a potential buyer. The buyer scrolls through the list to see product details and cost, and finally selects a product for purchase. Additional scrolling and selection occurs for the remainder of the list. As far as the buyer is concerned, the products appear one at a time, but the application uses a scrollable cursor to browse up and down through the result set.</span></span>

<span data-ttu-id="a3732-127">Il est possible d'utiliser les curseurs de diverses façons :</span><span class="sxs-lookup"><span data-stu-id="a3732-127">You can use cursors in a variety of ways:</span></span>

  - <span data-ttu-id="a3732-128">sans aucune ligne ;</span><span class="sxs-lookup"><span data-stu-id="a3732-128">With no rows at all.</span></span>

  - <span data-ttu-id="a3732-129">avec une partie ou l'ensemble des lignes d'une même table ;</span><span class="sxs-lookup"><span data-stu-id="a3732-129">With some or all of the rows in a single table.</span></span>

  - <span data-ttu-id="a3732-130">avec une partie ou l'ensemble des lignes issues de tables jointes de façon logique ;</span><span class="sxs-lookup"><span data-stu-id="a3732-130">With some or all of the rows from logically joined tables.</span></span>

  - <span data-ttu-id="a3732-131">en mode lecture seule ou actualisable, au niveau du curseur ou au niveau du champ ;</span><span class="sxs-lookup"><span data-stu-id="a3732-131">As read-only or updateable at the cursor or field level.</span></span>

  - <span data-ttu-id="a3732-132">en tant que curseur avant uniquement, ou avec défilement complet ;</span><span class="sxs-lookup"><span data-stu-id="a3732-132">As forward-only or fully scrollable.</span></span>

  - <span data-ttu-id="a3732-133">avec le jeu de clés du curseur situé sur le serveur ;</span><span class="sxs-lookup"><span data-stu-id="a3732-133">With the cursor keyset located on the server.</span></span>

  - <span data-ttu-id="a3732-134">sensibles aux modifications des tables sous-jacentes apportées par d'autres applications (appartenance, tri, insertion, mise à jour ou suppression) ;</span><span class="sxs-lookup"><span data-stu-id="a3732-134">Sensitive to underlying table changes caused by other applications (such as membership, sort, inserts, updates, and deletes).</span></span>

  - <span data-ttu-id="a3732-135">installés sur le serveur ou sur le client.</span><span class="sxs-lookup"><span data-stu-id="a3732-135">Existing on either the server or the client.</span></span>

<span data-ttu-id="a3732-p106">Les curseurs en lecture seule permettent de parcourir le jeu de résultats, alors que les curseurs en lecture/écriture peuvent appliquer des mises à jour de lignes individuelles. Vous pouvez définir des curseurs complexes avec des jeux de clés qui repointent vers les lignes des tables de base de données. Certains curseurs sont en lecture seule en direction avant, et d'autres peuvent avancer et reculer et permettent une actualisation dynamique du jeu de résultats en fonction des modifications apportées à la base de données par d'autres applications.</span><span class="sxs-lookup"><span data-stu-id="a3732-p106">Read-only cursors help users browse through the result set, and read/write cursors can implement individual row updates. Complex cursors can be defined with keysets that point back to base table rows. While some cursors are read-only in a forward direction, others can move back and forth and provide a dynamic refresh of the result set based on changes that other applications are making to the database.</span></span>

<span data-ttu-id="a3732-p107">Toutes les applications n'ont pas besoin de curseurs pour accéder aux données ou les mettre à jour. Certaines requêtes ne nécessitent pas de mise à jour directe de lignes à l'aide d'un curseur. Dans la mesure du possible, il ne faut utiliser les curseurs pour récupérer des données qu'en dernier recours et vous devez choisir le curseur dont l'impact est le plus limité possible. Lorsque vous créez un jeu de résultats à l'aide d'une procédure stockée, il n'est pas possible de mettre à jour le jeu de résultats en utilisant des méthodes de modification ou de mise à jour du curseur.</span><span class="sxs-lookup"><span data-stu-id="a3732-p107">Not all applications need to use cursors to access or update data. Some queries simply do not require direct row updating by using a cursor. Cursors should be one of the last techniques you choose to retrieve data — and then you should choose the lowest impact cursor possible. When you create a result set by using a stored procedure, the result set is not updateable using cursor edit or update methods.</span></span>

## <a name="concurrency"></a><span data-ttu-id="a3732-143">Accès simultané</span><span class="sxs-lookup"><span data-stu-id="a3732-143">Concurrency</span></span>

<span data-ttu-id="a3732-p108">Dans certaines applications multi-utilisateurs, il est essentiel que l'utilisateur final bénéficie de données à jour. Un système de réservation d'une compagnie aérienne constitue un exemple classique de ce type de système. En effet, il se peut que plusieurs utilisateurs souhaitent réserver le même siège sur un vol donné (lequel représente donc un enregistrement unique). Dans ce cas, l'application doit pouvoir gérer les éventuelles opérations simultanées effectuées sur un même enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a3732-p108">In some multi-user applications it is vitally important for the data presented to the end user to be as current as possible. A classic example of such a system is an airline reservation system, where many users might be contending for the same seat on a given flight (and thus, a single record). In a case like this, the application design must handle concurrent operations on a single record.</span></span>

<span data-ttu-id="a3732-p109">L'accès simultané ne constitue pas toujours un élément aussi important dans toutes les applications. Pour certaines d'entre elles, les dépenses encourues pour conserver à tout moment des données à jour ne se justifient pas.</span><span class="sxs-lookup"><span data-stu-id="a3732-p109">In other applications, concurrency is not as important. In such cases, the expense involved in keeping the data current at all times cannot be justified.</span></span>

## <a name="position"></a><span data-ttu-id="a3732-149">Position</span><span class="sxs-lookup"><span data-stu-id="a3732-149">Position</span></span>

<span data-ttu-id="a3732-p110">Un curseur assure également le suivi de la position active dans un jeu de résultats. La position du curseur doit être considérée comme un pointeur vers l'enregistrement actif, à l'instar d'un index de tableau pointant vers un emplacement spécifique du tableau.</span><span class="sxs-lookup"><span data-stu-id="a3732-p110">A cursor also keeps track of the current position in a result set. Think of the cursor position as a pointer to the current record, similar to the way an array index points to the value at that particular location in the array.</span></span>

## <a name="scrollability"></a><span data-ttu-id="a3732-152">Fonction de défilement</span><span class="sxs-lookup"><span data-stu-id="a3732-152">Scrollability</span></span>

<span data-ttu-id="a3732-153">Le type de curseur utilisé par votre application affecte également la possibilité de déplacer vers l’avant et arrière dans les lignes d’un jeu de résultats ; Il est parfois appelée fonction de défilement.</span><span class="sxs-lookup"><span data-stu-id="a3732-153">The type of cursor employed by your application also affects the ability to move forward and backward through the rows in a result set; this is sometimes called scrollability.</span></span> <span data-ttu-id="a3732-154">Possibilité de déplacer avant *et* arrière dans un jeu de résultats augmente la complexité du curseur et n’est donc plus coûteuse à implémenter.</span><span class="sxs-lookup"><span data-stu-id="a3732-154">The ability to move forward *and* backward through a result set adds to the complexity of the cursor, and is therefore more expensive to implement.</span></span> <span data-ttu-id="a3732-155">Pour cette raison, vous devez demander un curseur avec cette fonctionnalité uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a3732-155">For this reason, you should ask for a cursor with this functionality only when necessary.</span></span>

