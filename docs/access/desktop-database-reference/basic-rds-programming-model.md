---
title: Modèle de programmation RDS de base
TOCTitle: Basic RDS Programming Model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a90423f6bd05ae3d721faf97291ea6d21aa4393
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471000"
---
# <a name="basic-rds-programming-model"></a><span data-ttu-id="9e57e-102">Modèle de programmation RDS de base</span><span class="sxs-lookup"><span data-stu-id="9e57e-102">Basic RDS Programming Model</span></span>


<span data-ttu-id="9e57e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e57e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9e57e-p101">RDS est destiné aux applications qui existent dans l'environnement suivant : une application cliente spécifie un programme exécuté sur un serveur et les paramètres requis pour retourner les informations voulues. Le programme appelé sur le serveur accède à la source de données spécifiée, récupère les informations, traite éventuellement les données puis retourne les informations obtenues à l'application cliente sous une forme qu'elle peut facilement utiliser. RDS permet d'effectuer la séquence d'actions suivante :</span><span class="sxs-lookup"><span data-stu-id="9e57e-p101">RDS addresses applications that exist in the following environment: A client application specifies a program that will execute on a server and the parameters required to return the desired information. The program invoked on the server gains access to the specified data source, retrieves the information, optionally processes the data, and then returns the resulting information to your client application in a form that it can easily use. RDS provides the means for you to perform the following sequence of actions:</span></span>

  - <span data-ttu-id="9e57e-p102">Spécifier le programme à appeler sur le serveur et obtenir un moyen de s'y référer à partir du client. (Cette référence est parfois appelé *proxy* ; il s'agit du programme exécuté sur le serveur distant. L'application cliente « appelle » le proxy comme s'il s'agissait d'un programme local, mais elle appelle en réalité le programme sur le serveur distant.)</span><span class="sxs-lookup"><span data-stu-id="9e57e-p102">Specify the program to be invoked on the server, and obtain a way to refer to it from the client. (This reference is sometimes called a *proxy*. It represents the remote server program. The client application will "call" the proxy as if it were a local program, but it actually invokes the remote server program.)</span></span>

  - <span data-ttu-id="9e57e-p103">Appeler le programme sur le serveur et transmettre à ce programme des paramètres qui identifient la source de données et la commande à exécuter. (Le programme utilise en fait ADO pour accéder à la source de données. ADO établit une connexion avec le paramètre qui identifie la source de données, puis exécute la commande spécifiée par l'autre paramètre.)</span><span class="sxs-lookup"><span data-stu-id="9e57e-p103">Invoke the server program. Pass parameters to the server program that identify the data source and the command to issue. (The server program actually uses ADO to gain access to the data source. ADO makes a connection with one of the given parameters, and then issues the command specified in the other parameter.)</span></span>

  - <span data-ttu-id="9e57e-p104">Le programme sur le serveur obtient un objet [Recordset](recordset-object-ado.md) de la source de données. Le cas échéant, l'objet **Recordset** est traité sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="9e57e-p104">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source. Optionally, the **Recordset** object is processed on the server.</span></span>

  - <span data-ttu-id="9e57e-117">Le programme sur le serveur retourne l'objet **Recordset** final à l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="9e57e-117">The server program returns the final **Recordset** object to the client application.</span></span>

  - <span data-ttu-id="9e57e-118">Sur le client, l'objet **Recordset** est présenté sous une forme facilement utilisable par des contrôles visuels.</span><span class="sxs-lookup"><span data-stu-id="9e57e-118">On the client, the **Recordset** object is put into a form that can be easily used by visual controls.</span></span>

  - <span data-ttu-id="9e57e-119">Les modifications apportées à l'objet **Recordset** sont renvoyées au programme du serveur qui les utilise pour mettre à jour la source de données.</span><span class="sxs-lookup"><span data-stu-id="9e57e-119">Any modifications to the **Recordset** object are sent back to the server program, which uses them to update the data source.</span></span>

<span data-ttu-id="9e57e-p105">Ce modèle de programmation est pratique par certains aspects. Si vous n'avez pas besoin d'utiliser un programme complexe sur le serveur pour accéder à la source de données et si vous fournissez les paramètres de connexion et de commande requis, RDS récupère automatiquement les données spécifiées à l'aide d'un programme par défaut simple sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="9e57e-p105">This programming model contains certain convenience features. If you do not need a complex server program to access the data source, and if you provide the required connection and command parameters, RDS will automatically retrieve the specified data with a simple, default server program.</span></span>

<span data-ttu-id="9e57e-p106">Si un traitement plus complexe est nécessaire, vous pouvez spécifier votre propre programme personnalisé à utiliser sur le serveur. Par exemple, si un programme personnalisé sur le serveur bénéficie de toute la puissance d'ADO, il peut se connecter à différentes sources de données, combiner leurs données dans des opérations complexes, puis les retourner sous une forme simple et déjà traitée à l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="9e57e-p106">If you need more complex processing, you can specify your own custom server program. For example, because a custom server program has the full power of ADO at its disposal, it could connect to several different data sources, combine their data in some complex way, and then return a simple, processed result to the client application.</span></span>

<span data-ttu-id="9e57e-124">Enfin, si vous avez besoin d'un modèle de programmation à mi-chemin entre les deux exemples précédents, ADO permet à présent de personnaliser le comportement du programme serveur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9e57e-124">Finally, if your needs are somewhere in between, ADO now supports customizing the behavior of the default server program.</span></span>

