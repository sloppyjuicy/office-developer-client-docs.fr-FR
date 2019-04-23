---
title: Boutons de commande de Carnet d’adresses
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09f2513a3c541c76352e773f7f2a8f0c24f78850
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282477"
---
# <a name="address-book-command-buttons"></a><span data-ttu-id="a1811-102">Boutons de commande de Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="a1811-102">Address Book command buttons</span></span>


<span data-ttu-id="a1811-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1811-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a1811-104">L'application Carnet d'adresses comprend les boutons de commande suivants :</span><span class="sxs-lookup"><span data-stu-id="a1811-104">The Address Book application includes the following command buttons:</span></span>

- <span data-ttu-id="a1811-105">**Rechercher** pour envoyer une requête à la base de données ;</span><span class="sxs-lookup"><span data-stu-id="a1811-105">A **Find** button to submit a query to the database.</span></span>

- <span data-ttu-id="a1811-106">**Effacer** pour effacer les zones de texte avant de lancer une nouvelle recherche ;</span><span class="sxs-lookup"><span data-stu-id="a1811-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

- <span data-ttu-id="a1811-107">**Mettre à jour le profil** pour sauvegarder les modifications apportées à l'enregistrement d'un employé.</span><span class="sxs-lookup"><span data-stu-id="a1811-107">An **Update Profile** button to save changes to an employee record.</span></span>

- <span data-ttu-id="a1811-108">**Annuler les modifications** afin d'ignorer les modifications.</span><span class="sxs-lookup"><span data-stu-id="a1811-108">A **Cancel Changes** button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="a1811-109">Bouton Rechercher</span><span class="sxs-lookup"><span data-stu-id="a1811-109">Find Button</span></span>

<span data-ttu-id="a1811-110">Si vous cliquez sur le bouton **Rechercher** , la\_procédure VBScript Find OnClick Sub, qui génère et envoie la requête SQL, est activée.</span><span class="sxs-lookup"><span data-stu-id="a1811-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="a1811-111">La grille de données est alors remplie</span><span class="sxs-lookup"><span data-stu-id="a1811-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="a1811-112">Génération de la requête SQL</span><span class="sxs-lookup"><span data-stu-id="a1811-112">Building the SQL Query</span></span>

<span data-ttu-id="a1811-113">La première partie de la procédure\_Find OnClick Sub crée la requête SQL, une expression à la fois, en ajoutant des chaînes de texte à une instruction SQL SELECT globale.</span><span class="sxs-lookup"><span data-stu-id="a1811-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="a1811-114">Il commence par définir la variable sur une instruction SQL SELECT qui demande toutes les lignes de données de la table de source de données.</span><span class="sxs-lookup"><span data-stu-id="a1811-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="a1811-115">La procédure Sub analyse ensuite chacune des quatre zones de texte de la page.</span><span class="sxs-lookup"><span data-stu-id="a1811-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="a1811-116">Étant donné que le programme utilise le mot dans la création des instructions SQL, les requêtes sont des recherches de sous-chaînes plutôt que des correspondances exactes.</span><span class="sxs-lookup"><span data-stu-id="a1811-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="a1811-117">Par exemple, si la zone **nom** contient l'entrée «Berge» et que la zone **titre** contient l'entrée «Program Manager», l'instruction SQL (value of) lirait:</span><span class="sxs-lookup"><span data-stu-id="a1811-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="a1811-118">Si la requête aboutit, toutes les personnes, dont le nom de famille contient le texte « Berge » (par exemple Berge ou Berger) et dont la fonction contient les termes « Program Manager » (par exemple Program Manager, Advanced Technologies)  sont affichées dans la grille de données HTML.</span><span class="sxs-lookup"><span data-stu-id="a1811-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="a1811-119">Préparation et envoi de la requête</span><span class="sxs-lookup"><span data-stu-id="a1811-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="a1811-120">La dernière partie de la procédure\_Find OnClick Sub est composée de deux instructions.</span><span class="sxs-lookup"><span data-stu-id="a1811-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="a1811-121">La première instruction affecte la propriété SQL de l'objet RDS. DataControl est égal à la requête SQL générée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="a1811-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="a1811-122">La deuxième instruction provoque l' **objet RDS. DataControl** () pour interroger la base de données, puis afficher les nouveaux résultats de la requête dans la grille.</span><span class="sxs-lookup"><span data-stu-id="a1811-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="a1811-123">Mettre à jour le profil</span><span class="sxs-lookup"><span data-stu-id="a1811-123">Update Profile Button</span></span>

<span data-ttu-id="a1811-124">Si vous cliquez sur le bouton **mettre à jour** le\_profil, la procédure de mise à jour OnClick de VBScript, qui exécute l'objet RDS, est activée. DataControl () de l'objet () SubmitChanges et Refresh.</span><span class="sxs-lookup"><span data-stu-id="a1811-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="a1811-125">Lorsque DC1. SubmitChanges s'exécute, le service de données à distance regroupe toutes les informations de mise à jour et les envoie au serveur via HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1811-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="a1811-126">La mise à jour est tout-ou-rien; Si une partie de la mise à jour échoue, aucune des modifications n'est apportée et un message d'État est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="a1811-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="a1811-127">s'exécute, le service de données à distance transmet toutes les informations de mise à jour et les envoie au serveur via HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1811-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="a1811-128">La mise à jour est tout-ou-rien; Si une partie de la mise à jour échoue, aucune des modifications n'est apportée et un message d'État est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="a1811-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="a1811-129">DC1. L'actualisation n'est pas nécessaire après **SubmitChanges** avec le service de données à distance, mais elle garantit des données actualisées.</span><span class="sxs-lookup"><span data-stu-id="a1811-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="a1811-130">Bouton Annuler les modifications</span><span class="sxs-lookup"><span data-stu-id="a1811-130">Cancel Changes Button</span></span>

<span data-ttu-id="a1811-131">Le fait de cliquer sur **annuler les modifications** active la sous-procédure VBScript Cancel\_OnClick OnClick, qui exécute l'objet RDS. DataControl (méthode CancelUpdate).</span><span class="sxs-lookup"><span data-stu-id="a1811-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="a1811-132">Quand il s'exécute, il rejette toutes les modifications qu'un utilisateur a apportées à un enregistrement d'employé dans la grille de données depuis la dernière requête ou mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a1811-132">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update.</span></span> <span data-ttu-id="a1811-133">Elle restaure les valeurs d'origine.</span><span class="sxs-lookup"><span data-stu-id="a1811-133">It restores the original values.</span></span>

