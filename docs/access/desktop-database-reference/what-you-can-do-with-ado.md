---
title: Avantages et possibilités d'ADO
TOCTitle: What You Can Do With ADO
ms:assetid: 98246cb0-aec6-6a77-c953-85895ad83a5d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249681(v=office.15)
ms:contentKeyID: 48546483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d944d70e7aba054abb7e6f02933b1311bb90ee17
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469489"
---
# <a name="what-you-can-do-with-ado"></a><span data-ttu-id="63f58-102">Avantages et possibilités d'ADO</span><span class="sxs-lookup"><span data-stu-id="63f58-102">What You Can Do With ADO</span></span>


<span data-ttu-id="63f58-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="63f58-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="63f58-p101">ADO fournit aux développeurs un modèle objet d'une puissance et d'une logique remarquables. Il permet d'accéder, de modifier et de mettre à jour par programme un grand nombre de sources de données via les interfaces système OLE DB. L'utilisation la plus fréquente d'ADO consiste à exécuter des requêtes sur une ou plusieurs tables d'une base de données relationnelle, à extraire et à afficher les résultats dans une application et, le cas échéant, à permettre aux utilisateurs de modifier les données et d'enregistrer ces modifications. Mais ADO permet également d'effectuer d'autres opérations par programme :</span><span class="sxs-lookup"><span data-stu-id="63f58-p101">ADO is designed to provide developers with a powerful, logical object model for programmatically accessing, editing, and updating a wide variety of data sources through OLE DB system interfaces. The most common usage of ADO is to query a table or tables in a relational database, retrieve and display the results in an application, and perhaps allow users to make and save changes to the data. Other things that can be done programmatically with ADO include:</span></span>

  - <span data-ttu-id="63f58-107">Exécuter des requêtes SQL dans une base de données, et afficher les résultats correspondants</span><span class="sxs-lookup"><span data-stu-id="63f58-107">Querying a database using SQL and displaying the results.</span></span>

  - <span data-ttu-id="63f58-108">Accéder à des informations d'un magasin de fichiers sur Internet</span><span class="sxs-lookup"><span data-stu-id="63f58-108">Accessing information in a file store over the Internet.</span></span>

  - <span data-ttu-id="63f58-109">Manipuler les messages et les dossiers d'un système de messagerie électronique</span><span class="sxs-lookup"><span data-stu-id="63f58-109">Manipulating messages and folders in an e-mail system.</span></span>

  - <span data-ttu-id="63f58-110">Enregistrer des données d'une base de données dans un fichier XML</span><span class="sxs-lookup"><span data-stu-id="63f58-110">Saving data from a database into an XML file.</span></span>

  - <span data-ttu-id="63f58-111">Permettre aux utilisateurs d'examiner et de modifier les données dans des tables de bases de données</span><span class="sxs-lookup"><span data-stu-id="63f58-111">Allowing a user to review and make changes to data in database tables.</span></span>

  - <span data-ttu-id="63f58-112">Créer et réutiliser des commandes de base de données paramétrées</span><span class="sxs-lookup"><span data-stu-id="63f58-112">Creating and reusing parameterized database commands.</span></span>

  - <span data-ttu-id="63f58-113">Exécuter des procédures stockées</span><span class="sxs-lookup"><span data-stu-id="63f58-113">Executing stored procedures.</span></span>

  - <span data-ttu-id="63f58-114">Créer dynamiquement une structure flexible appelée **jeu d'enregistrements** pour le stockage, la navigation et la manipulation des données</span><span class="sxs-lookup"><span data-stu-id="63f58-114">Dynamically creating a flexible structure, called a **Recordset**, to hold, navigate, and manipulate data.</span></span>

  - <span data-ttu-id="63f58-115">Effectuer des opérations de base de données transactionnelle</span><span class="sxs-lookup"><span data-stu-id="63f58-115">Performing transactional database operations.</span></span>

  - <span data-ttu-id="63f58-116">Filtrer et trier des copies locales d'informations de base de données selon des critères d'exécution</span><span class="sxs-lookup"><span data-stu-id="63f58-116">Filtering and sorting local copies of database information based on run-time criteria.</span></span>

  - <span data-ttu-id="63f58-117">Créer et manipuler des résultats hiérarchiques de bases de données</span><span class="sxs-lookup"><span data-stu-id="63f58-117">Creating and manipulating hierarchical results from databases.</span></span>

  - <span data-ttu-id="63f58-118">Lier des champs de base de données à des composants liés aux bases de données</span><span class="sxs-lookup"><span data-stu-id="63f58-118">Binding database fields to data-aware components.</span></span>

  - <span data-ttu-id="63f58-119">Créer des **jeux d'enregistrements** distants et non connectés</span><span class="sxs-lookup"><span data-stu-id="63f58-119">Creating remote, disconnected **Recordsets**.</span></span>

<span data-ttu-id="63f58-p102">ADO doit exposer une grande variété d'options et de paramètres pour offrir une telle flexibilité. Par conséquent, il est essentiel d'adopter une approche méthodique de l'utilisation d'ADO dans une application, et de structurer vos objectifs en les scindant en éléments gérables.</span><span class="sxs-lookup"><span data-stu-id="63f58-p102">ADO must expose a wide variety of options and settings in order to provide such flexibility. Therefore it's important to take a methodical approach to learning how to use ADO in an application, breaking down each of your goals into manageable pieces.</span></span>

<span data-ttu-id="63f58-p103">Les programmes ADO impliquent quatre opérations essentielles : l'accès, l'analyse, la modification et la mise à jour des données. Ces quatre opérations sont présentées en détail dans les quatre chapitres suivants.</span><span class="sxs-lookup"><span data-stu-id="63f58-p103">Four primary operations are involved in most ADO programs: getting data, examining data, editing data, and updating data. The next four chapters examine each of these operations in more detail.</span></span>

<span data-ttu-id="63f58-p104">Avant de commencer, familiarisez-vous avec les objets du modèle objet ADO. Passez ensuite à la rubrique [HelloData : une application ADO simple](hellodata-a-simple-ado-application.md). Cette application est écrite en Visual Basic et permet l'exécution des quatre principales opérations d'ADO.</span><span class="sxs-lookup"><span data-stu-id="63f58-p104">Before proceeding, familiarize yourself with the objects in the ADO Object Model. Then review [HelloData: A Simple ADO Application](hellodata-a-simple-ado-application.md). This application is written in Visual Basic and performs each of the four primary ADO operations.</span></span>

