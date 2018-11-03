---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d55fd58daf13fa0f3995480f35da4ccc0f17ac5c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946684"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="d490b-102">À l’aide de l’objet Command (accès)</span><span class="sxs-lookup"><span data-stu-id="d490b-102">Using the Command object (Access)</span></span>


<span data-ttu-id="d490b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d490b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d490b-p101">Une fois connecté à une source de données, vous devez y exécuter des requêtes pour obtenir des jeux de résultats. ADO encapsule ce type de fonctionnalité de commande dans l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="d490b-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="d490b-p102">Vous pouvez utiliser l'objet **Command** pour demander au fournisseur n'importe quel type d'opération, à condition que ce dernier puisse interpréter correctement la chaîne de commande. Une des opérations courantes pour les fournisseurs de données est l'interrogation d'une base de données et le renvoi des enregistrements correspondants dans un objet **Recordset**. Les objets **Recordset** seront présentés plus loin dans ce chapitre et dans d'autres chapitres. Considérons-les pour l'instant comme des outils permettant de stocker et d'afficher des jeux de résultats. Comme pour un certain nombre d'objets ADO, selon les fonctionnalités offertes par le fournisseur, la référence à certaines collections, méthodes ou propriétés de l'objet **Command** peut générer des erreurs.</span><span class="sxs-lookup"><span data-stu-id="d490b-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="d490b-p103">Il n'est pas toujours nécessaire de créer un objet **Command** pour exécuter une commande sur une source de données. Vous pouvez utiliser la méthode **Execute** sur l'objet **Connection**, ou la méthode **Open** sur l'objet **Recordset**. Toutefois, vous devez impérativement utiliser un objet **Command** si vous devez réutiliser une commande dans votre code ou si vous devez transmettre des informations de paramétrage avec votre commande. Ces scénarios sont présentés en détail dans une autre section du présent chapitre.</span><span class="sxs-lookup"><span data-stu-id="d490b-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="d490b-114">Certaines commandes peuvent renvoyer un résultat sous forme de flux binaire ou en tant qu’un seul enregistrement au lieu d’un jeu d’enregistrements, si cela est pris en charge par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d490b-114">Certain Commands can return a result set as a binary stream or as a single Record rather than as a Recordset, if this is supported by the provider.</span></span> <span data-ttu-id="d490b-115">En outre, certaines commandes ne sont pas destinés à renvoyer de jeu de résultats (par exemple, une requête SQL Update).</span><span class="sxs-lookup"><span data-stu-id="d490b-115">Also, some Commands are not intended to return any result set at all (for example, a SQL Update query).</span></span> <span data-ttu-id="d490b-116">Ce chapitre présente le scénario le plus courant, toutefois : exécution des commandes qui retournent des résultats dans un objet Recordset.</span><span class="sxs-lookup"><span data-stu-id="d490b-116">This chapter will cover the most typical scenario, however: executing Commands that return results into a Recordset object.</span></span> <span data-ttu-id="d490b-117">Pour plus d’informations sur le renvoi des résultats en enregistrements ou en flux, voir [chapitre 10 : enregistrements et flux](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="d490b-117">For more information about returning results into Records or Streams, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

<span data-ttu-id="d490b-118">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d490b-118">This section includes the following topics:</span></span>

- [<span data-ttu-id="d490b-119">Vue d’ensemble de l’objet Command</span><span class="sxs-lookup"><span data-stu-id="d490b-119">Command Object Overview</span></span>](command-object-overview.md)

- [<span data-ttu-id="d490b-120">Création et exécution d’une commande simple</span><span class="sxs-lookup"><span data-stu-id="d490b-120">Creating and Executing a Simple Command</span></span>](creating-and-executing-a-simple-command.md)

- [<span data-ttu-id="d490b-121">Paramètres de l’objet Command</span><span class="sxs-lookup"><span data-stu-id="d490b-121">Command Object Parameters</span></span>](command-object-parameters.md)

- [<span data-ttu-id="d490b-122">Appel d’une procédure stockée à l’aide d’une commande</span><span class="sxs-lookup"><span data-stu-id="d490b-122">Calling a Stored Procedure with a Command</span></span>](calling-a-stored-procedure-with-a-command.md)

- [<span data-ttu-id="d490b-123">Commandes nommées</span><span class="sxs-lookup"><span data-stu-id="d490b-123">Named Commands</span></span>](named-commands.md)
