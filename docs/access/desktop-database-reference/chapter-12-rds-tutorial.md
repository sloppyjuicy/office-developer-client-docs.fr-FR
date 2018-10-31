---
title: 'Chapitre 12 : Didacticiel RDS'
TOCTitle: 'Chapter 12: RDS Tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aec7c9a89ea078bfad9b05d664d373831491edc4
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860223"
---
# <a name="chapter-12-rds-tutorial"></a><span data-ttu-id="33cd3-102">Chapitre 12 : Didacticiel RDS</span><span class="sxs-lookup"><span data-stu-id="33cd3-102">Chapter 12: RDS Tutorial</span></span>


<span data-ttu-id="33cd3-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="33cd3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="33cd3-p101">Ce didacticiel illustre l'utilisation du modèle de programmation RDS pour interroger et mettre à jour une source de données. Dans un premier temps, il décrit les étapes à suivre pour accomplir cette tâche. Ensuite, le didacticiel est reproduit dans Microsoft® Visual Basic Scripting Edition et Microsoft® Visual J++®, avec ADO for Windows Foundation Classes (ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="33cd3-p101">This tutorial illustrates using the RDS programming model to query and update a data source. First, it describes the steps necessary to accomplish this task. Then the tutorial is repeated in Microsoft® Visual Basic Scripting Edition and Microsoft® Visual J++®, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="33cd3-107">Ce didacticiel est codé dans différents langages pour deux raisons :</span><span class="sxs-lookup"><span data-stu-id="33cd3-107">This tutorial is coded in different languages for two reasons:</span></span>

  - <span data-ttu-id="33cd3-p102">La documentation portant sur RDS part du principe que le lecteur code en Visual Basic. Si cette documentation s'avère utile pour les programmeurs qui codent en Visual Basic, elle l'est moins pour les programmeurs qui utilisent d'autres langages.</span><span class="sxs-lookup"><span data-stu-id="33cd3-p102">The documentation for RDS assumes the reader codes in Visual Basic. This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

  - <span data-ttu-id="33cd3-110">Si vous avez un doute concernant une fonctionnalité RDS déterminée et que vous possédez certaines connaissances dans un autre langage, vous pouvez éventuellement résoudre votre problème en examinant cette même fonction exprimée dans un autre langage.</span><span class="sxs-lookup"><span data-stu-id="33cd3-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

## <a name="how-the-tutorial-is-presented"></a><span data-ttu-id="33cd3-111">Présentation du didacticiel</span><span class="sxs-lookup"><span data-stu-id="33cd3-111">How the Tutorial is Presented</span></span>

<span data-ttu-id="33cd3-p103">Ce didacticiel est basé sur le modèle de programmation RDS. Chaque étape du modèle de programmation y est abordée, avec en outre une illustration de chacune de ces étapes par un fragment de code Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="33cd3-p103">This tutorial is based on the RDS programming model. It discusses each step of the programming model individually. In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="33cd3-p104">L'exemple de code est reproduit dans les autres langages avec un minimum de détails. Chaque étape figurant dans le didacticiel d'un langage de programmation donné s'accompagne d'une mention de l'étape correspondante dans le modèle de programmation et le didacticiel descriptif. Servez-vous du numéro de l'étape pour accéder aux détails correspondants dans le didacticiel descriptif.</span><span class="sxs-lookup"><span data-stu-id="33cd3-p104">The code example is repeated in other languages with minimal discussion. Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial. Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="33cd3-p105">Le modèle de programmation RDS est indiqué ci-dessous. Référez-vous-y à mesure que vous avancez dans le didacticiel.</span><span class="sxs-lookup"><span data-stu-id="33cd3-p105">The RDS programming model is stated below. Use it as a roadmap as you proceed through the tutorial.</span></span>

## <a name="rds-programming-model-with-objects"></a><span data-ttu-id="33cd3-120">Modèle de programmation RDS avec objets</span><span class="sxs-lookup"><span data-stu-id="33cd3-120">RDS Programming Model with Objects</span></span>

  - <span data-ttu-id="33cd3-121">Spécifiez le programme à appeler sur le serveur et obtenir un moyen (proxy) d'y faire référence à partir du client.</span><span class="sxs-lookup"><span data-stu-id="33cd3-121">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

  - <span data-ttu-id="33cd3-p106">Appelez le programme serveur. Transmettez les paramètres au programme serveur qui identifie la source de données et la commande à émettre.</span><span class="sxs-lookup"><span data-stu-id="33cd3-p106">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

  - <span data-ttu-id="33cd3-p107">Le programme serveur obtient un objet [Recordset](recordset-object-ado.md) auprès de la source de données, généralement en utilisant ADO. L'objet **Recordset** peut éventuellement être traité sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="33cd3-p107">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server.</span></span>

  - <span data-ttu-id="33cd3-126">Le programme serveur retourne l'objet **Recordset** final à l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="33cd3-126">The server program returns the final **Recordset** object to the client application.</span></span>

  - <span data-ttu-id="33cd3-127">Au niveau du client, l'objet **Recordset** est éventuellement placé dans un format facilement exploitable par des contrôles visuels.</span><span class="sxs-lookup"><span data-stu-id="33cd3-127">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

  - <span data-ttu-id="33cd3-128">Les modifications apportées à l'objet **Recordset** sont renvoyées au serveur et utilisées pour la mise à jour de la source de données.</span><span class="sxs-lookup"><span data-stu-id="33cd3-128">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

<span data-ttu-id="33cd3-129">Voici les étapes décrites dans ce didacticiel :</span><span class="sxs-lookup"><span data-stu-id="33cd3-129">Following are the steps in this tutorial:</span></span>

- [<span data-ttu-id="33cd3-130">Étape 1 : Spécifier un programme serveur (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="33cd3-130">Step 1: Specify a Server Program (RDS Tutorial)</span></span>](step-1-specify-a-server-program-rds-tutorial.md)

- [<span data-ttu-id="33cd3-131">Étape 2 : Appeler le programme serveur (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="33cd3-131">Step 2: Invoke the Server Program (RDS Tutorial)</span></span>](step-2-invoke-the-server-program-rds-tutorial.md)

- [<span data-ttu-id="33cd3-132">Étape 3 : Le serveur obtient un recordset (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="33cd3-132">Step 3: Server Obtains a Recordset (RDS Tutorial)</span></span>](step-3-server-obtains-a-recordset-rds-tutorial.md)

- [<span data-ttu-id="33cd3-133">Étape 4 : Le serveur renvoie le recordset (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="33cd3-133">Step 4: Server Returns the Recordset (RDS Tutorial)</span></span>](step-4-server-returns-the-recordset-rds-tutorial.md)

- [<span data-ttu-id="33cd3-134">Étape 5 : DataControl est disponible (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="33cd3-134">Step 5: DataControl is Made Usable (RDS Tutorial)</span></span>](step-5-datacontrol-is-made-usable-rds-tutorial.md)

- [<span data-ttu-id="33cd3-135">Étape 6 : Modifications envoyées au serveur (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="33cd3-135">Step 6: Changes are Sent to the Server (RDS Tutorial)</span></span>](step-6-changes-are-sent-to-the-server-rds-tutorial.md)

- [<span data-ttu-id="33cd3-136">Didacticiel RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="33cd3-136">RDS Tutorial (VBScript)</span></span>](rds-tutorial-vbscript.md)

- [<span data-ttu-id="33cd3-137">Didacticiel RDS (Visual J++)</span><span class="sxs-lookup"><span data-stu-id="33cd3-137">RDS Tutorial (Visual J++)</span></span>](rds-tutorial-visual-j.md)