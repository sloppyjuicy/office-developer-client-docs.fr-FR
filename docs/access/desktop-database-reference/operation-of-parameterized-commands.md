---
title: Fonctionnement des commandes paramétrées
TOCTitle: Operation of parameterized commands
ms:assetid: 71edbd16-21db-7afa-356b-d8e7afb92b3a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249456(v=office.15)
ms:contentKeyID: 48545596
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 145a2ee6c3d3c614eb9660350a0bb8a00d44d04c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288286"
---
# <a name="operation-of-parameterized-commands"></a><span data-ttu-id="b4806-102">Fonctionnement des commandes paramétrées</span><span class="sxs-lookup"><span data-stu-id="b4806-102">Operation of parameterized commands</span></span>

<span data-ttu-id="b4806-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4806-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4806-104">Si vous utilisez un **jeu d'enregistrements** enfant de taille imposante, notamment par rapport à celle du **jeu d'enregistrements** parent, mais que vous n'avez besoin d'accéder qu'à un nombre réduit de chapitres enfant, nous vous conseillons d'utiliser une commande paramétrée.</span><span class="sxs-lookup"><span data-stu-id="b4806-104">If you are working with a large child **Recordset**, especially compared to the size of the parent **Recordset**, but need to access only a few child chapters, you might find it more efficient to use a parameterized command.</span></span>

<span data-ttu-id="b4806-105">Une *commande non paramétrée* extrait l'intégralité des **jeux d'enregistrements** enfant et parent, ajoute une colonne de chapitre au parent, puis affecte une référence au chapitre enfant associé de chaque ligne parent.</span><span class="sxs-lookup"><span data-stu-id="b4806-105">A *non-parameterized command* retrieves both the entire parent and child **Recordsets**, appends a chapter column to the parent, and then assigns a reference to the related child chapter for each parent row.</span></span>

<span data-ttu-id="b4806-p101">Une *commande paramétrée* extrait l'intégralité du **jeu d'enregistrements** parent, mais n'extrait le **jeu d'enregistrements** de chapitre que lorsque vous accédez à la colonne de chapitre. Cette différence dans la méthode d'extraction apporte des améliorations considérables en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="b4806-p101">A *parameterized command* retrieves the entire parent **Recordset**, but retrieves only the chapter **Recordset** when the chapter column is accessed. This difference in retrieval strategy can yield significant performance benefits.</span></span>

<span data-ttu-id="b4806-108">Vous pouvez par exemple spécifier ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b4806-108">For example, you can specify the following:</span></span>

```vb 
 
SHAPE {SELECT * FROM customer} 
 APPEND ({SELECT * FROM orders WHERE cust_id = ?} 
 RELATE cust_id TO PARAMETER 0) 
```

<span data-ttu-id="b4806-109">Les tables parent et enfant ont un nom de colonne en commun,\_ID client *.*</span><span class="sxs-lookup"><span data-stu-id="b4806-109">The parent and child tables have a column name in common, cust\_id *.*</span></span> <span data-ttu-id="b4806-110">La *commande Child* a un espace réservé «?» auquel la clause relate fait référence (c'est-à-dire, «... PARAMÈTRE 0).</span><span class="sxs-lookup"><span data-stu-id="b4806-110">The *child-command* has a "?" placeholder, to which the RELATE clause refers (that is, "...PARAMETER 0").</span></span>

> [!NOTE]
> <span data-ttu-id="b4806-p103">[!REMARQUE] La clause PARAMETER appartient uniquement à la syntaxe de commande de mise en forme. Elle n'est associée ni à l'objet [Parameter](parameter-object-ado.md), ni à la collection [Parameters](parameters-collection-ado.md) ADO.</span><span class="sxs-lookup"><span data-stu-id="b4806-p103">The PARAMETER clause pertains solely to the shape command syntax. It is not associated with either the ADO [Parameter](parameter-object-ado.md) object or the [Parameters](parameters-collection-ado.md) collection.</span></span>

<span data-ttu-id="b4806-113">Lors de l'exécution de la commande de mise en forme paramétrée, l'opération suivante se produit :</span><span class="sxs-lookup"><span data-stu-id="b4806-113">When the parameterized shape command is executed, the following occurs:</span></span>

1.  <span data-ttu-id="b4806-114">La *commande-parent* est exécutée et renvoie un **jeu d'enregistrements** parent de la table Customers.</span><span class="sxs-lookup"><span data-stu-id="b4806-114">The *parent-command* is executed and returns a parent **Recordset** from the Customers table.</span></span>

2.  <span data-ttu-id="b4806-115">Une colonne de chapitre est ajoutée au **jeu d'enregistrements** parent.</span><span class="sxs-lookup"><span data-stu-id="b4806-115">A chapter column is appended to the parent **Recordset**.</span></span>

3.  <span data-ttu-id="b4806-116">Lorsque vous accédez à la colonne de chapitre d'une ligne parente, la *commande Child-Command* est exécutée à l'aide\_de la valeur de l'ID Customer. cust comme valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="b4806-116">When the chapter column of a parent row is accessed, the *child-command* is executed using the value of the customer.cust\_id as the value of the parameter.</span></span>

4.  <span data-ttu-id="b4806-117">Toutes les lignes du jeu de lignes du fournisseur de données créées à l’étape 3 sont utilisées pour renseigner le **jeu d’enregistrements** enfant.</span><span class="sxs-lookup"><span data-stu-id="b4806-117">All rows in the data provider rowset created in step 3 are used to populate the child **Recordset**.</span></span> <span data-ttu-id="b4806-118">Dans cet exemple, il s'agit de toutes les lignes de la table Orders dont\_l'ID cust est égal à la valeur de\_Customer. Customer ID.</span><span class="sxs-lookup"><span data-stu-id="b4806-118">In this example, that is all the rows in the Orders table in which the cust\_id equals the value of customer.cust\_id.</span></span> <span data-ttu-id="b4806-119">Par défaut, les **jeux d’enregistrements** enfant sont mis en cache sur le client jusqu’à ce que toutes les références au **jeu d’enregistrements** parent soient extraites.</span><span class="sxs-lookup"><span data-stu-id="b4806-119">By default, the child **Recordset**s will be cached on the client until all references to the parent **Recordset** are released.</span></span> <span data-ttu-id="b4806-120">Pour modifier ce comportement, affectez la **valeur false**aux**lignes enfants du cache** de [propriétés dynamiques](ado-dynamic-property-index.md)du **jeu d'enregistrements** .</span><span class="sxs-lookup"><span data-stu-id="b4806-120">To change this behavior, set the **Recordset** [dynamic property](ado-dynamic-property-index.md)**Cache Child Rows** to **False**.</span></span>

5.  <span data-ttu-id="b4806-121">Une référence aux lignes enfant extraites (c'est-à-dire le chapitre du **jeu d'enregistrements** enfant) est placée dans la colonne de chapitre de la ligne active du **jeu d'enregistrements** parent.</span><span class="sxs-lookup"><span data-stu-id="b4806-121">A reference to the retrieved child rows (that is, the chapter of the child **Recordset**) is placed in the chapter column of the current row of the parent **Recordset**.</span></span>

6.  <span data-ttu-id="b4806-122">Les étapes 3 à 5 sont répétées lorsque vous accédez à la colonne de chapitre d'une autre ligne.</span><span class="sxs-lookup"><span data-stu-id="b4806-122">Steps 3–5 are repeated when the chapter column of another row is accessed.</span></span>

<span data-ttu-id="b4806-p105">La propriété dynamique **Cache Child Rows** est définie sur **True** par défaut. Le comportement de mise en cache varie en fonction des valeurs de paramètre de la requête. Dans une requête à paramètre unique, le **jeu d'enregistrements** enfant d'une valeur de paramètre donnée est mis en cache entre les requêtes pour un enfant avec la même valeur. Ceci est illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="b4806-p105">The **Cache Child Rows** dynamic property is set to **True** by default. The caching behavior varies depending upon the parameter values of the query. In a query with a single parameter, the child **Recordset** for a given parameter value will be cached between requests for a child with that value. The following code demonstrates this:</span></span>

```vb
... 
SCmd = "SHAPE {select * from customer} " & _ 
 "APPEND({select * from orders where cust_id = ?} " & _ 
 "RELATE cust_id TO PARAMETER 0) AS chpCustOrder" 
Rst1.Open sCmd, Cnn1 
Set RstChild = Rst1("chpCustOrder").Value 
Rst1.MoveNext ' Next cust_id passed to Param 0, & new rs fetched 
 ' into RstChild. 
Rst1.MovePrevious ' RstChild now holds cached rs, saving round trip. 
... 
```

<span data-ttu-id="b4806-127">Dans une requête avec deux paramètres ou plus, un enfant mis en cache est utilisé uniquement si toutes les valeurs de paramètre correspondent aux valeurs mises en cache.</span><span class="sxs-lookup"><span data-stu-id="b4806-127">In a query with two or more parameters, a cached child is used only if all the parameter values match the cached values.</span></span>

## <a name="parameterized-commands-and-complex-parent-child-relations"></a><span data-ttu-id="b4806-128">Commandes paramétrées et relations enfants complexes</span><span class="sxs-lookup"><span data-stu-id="b4806-128">Parameterized commands and complex parent child relations</span></span>

<span data-ttu-id="b4806-129">Les commandes paramétrées permettent non seulement d'améliorer les performances en terme de hiérarchie de type équi-jointure, mais elles peuvent également être utilisées pour la prise en charge de relations parent-enfant plus complexes.</span><span class="sxs-lookup"><span data-stu-id="b4806-129">In addition to using parameterized commands to improve performance of an equi-join type hierarchy, parameterized commands can be used to support more complex parent-child relationships.</span></span> <span data-ttu-id="b4806-130">Par exemple, considérez une base de données de la ligue avec deux tables: une qui se\_compose des équipes\_(ID d'équipe, nom de l'équipe) et\_l'autre des\_jeux (date, équipe d'accueil, équipe de visite).</span><span class="sxs-lookup"><span data-stu-id="b4806-130">For example, consider a Little League database with two tables: one consisting of the teams (team\_id, team\_name) and the other of games (date, home\_team, visiting\_team).</span></span>

<span data-ttu-id="b4806-131">Avec une hiérarchie non paramétrée, vous ne pouvez en aucun cas relier les deux tables de telle sorte que le **jeu d'enregistrements** enfant de chaque équipe contienne l'ensemble de son calendrier.</span><span class="sxs-lookup"><span data-stu-id="b4806-131">Using a non-parameterized hierarchy, there is no way to relate the teams and games tables in such a way that the child **Recordset** for each team contains its complete schedule.</span></span> <span data-ttu-id="b4806-132">Vous pouvez créer des chapitres contenant le calendrier à domicile ou le calendrier à l'extérieur, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="b4806-132">You can create chapters that contain the home schedule or the road schedule, but not both.</span></span> <span data-ttu-id="b4806-133">Ceci s'explique par le fait que la clause RELATE vous limite à des relations parent-enfant de type (pc1=cc1) AND (pc2=pc2).</span><span class="sxs-lookup"><span data-stu-id="b4806-133">This is because the RELATE clause limits you to parent-child relationships of the form (pc1=cc1) AND (pc2=pc2).</span></span> <span data-ttu-id="b4806-134">PAR conséquent, si votre commande inclut «associer\_l'ID d'\_équipe à l'\_équipe personnelle,\_l'ID d'équipe à l'équipe de visite», vous n'obtiendrez que les jeux dans lesquels une équipe s'était jouée.</span><span class="sxs-lookup"><span data-stu-id="b4806-134">So, if your command included "RELATE team\_id TO home\_team, team\_id TO visiting\_team", you would get only games where a team was playing itself.</span></span> <span data-ttu-id="b4806-135">Ce que vous souhaitez est «(\_ID d'équipe\_= Accueil Team) ou\_(ID d'\_équipe = équipe de visite)», mais le fournisseur de formes ne prend pas en charge la clause or.</span><span class="sxs-lookup"><span data-stu-id="b4806-135">What you want is "(team\_id=home\_team) OR (team\_id=visiting\_team)", but the Shape provider does not support the OR clause.</span></span>

<span data-ttu-id="b4806-p108">Pour obtenir le résultat souhaité, vous pouvez utiliser une commande paramétrée. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b4806-p108">To obtain the desired result, you can use a parameterized command. For example:</span></span>

```vb 
 
SHAPE {SELECT * FROM teams} 
APPEND ({SELECT * FROM games WHERE home_team = ? OR visiting_team = ?} 
 RELATE team_id TO PARAMETER 0, 
 team_id TO PARAMETER 1) 
```

<span data-ttu-id="b4806-138">Cet exemple exploite la plus grande flexibilité de la clause SQL WHERE pour obtenir le résultat escompté.</span><span class="sxs-lookup"><span data-stu-id="b4806-138">This example exploits the greater flexibility of the SQL WHERE clause to get the result you need.</span></span>

