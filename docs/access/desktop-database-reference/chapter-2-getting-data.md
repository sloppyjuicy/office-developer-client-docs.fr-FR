---
title: 'Chapitre 2 : Obtention de données'
TOCTitle: 'Chapter 2: Getting Data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 601d18373f5bcd0a9ed6777fa50c2a3ed631594a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860888"
---
# <a name="chapter-2-getting-data"></a><span data-ttu-id="89ac5-102">Chapitre 2 : Obtention de données</span><span class="sxs-lookup"><span data-stu-id="89ac5-102">Chapter 2: Getting Data</span></span>


<span data-ttu-id="89ac5-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="89ac5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="89ac5-p101">Le chapitre précédent a présenté les quatre opérations primaires impliquées dans la création d'une application ADO : l'extraction des données, l'examen des données, la modification des données et la mise à jour des données. Ce chapitre va se pencher plus en détail sur les concepts relatifs à la première opération : l'extraction des données.</span><span class="sxs-lookup"><span data-stu-id="89ac5-p101">The preceding chapter introduced four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data. This chapter will focus on the details of the concepts relevant to the first operation: getting data.</span></span>

<span data-ttu-id="89ac5-p102">Plusieurs objets ADO peuvent jouer un rôle dans cette opération. Tout d'abord, vous vous connectez à la source de données à l'aide d'un objet **Connection** ADO (qui est parfois créé de manière implicite). Ensuite, vous transmettez vos instructions à la source de données à l'aide d'un objet **Command** ADO (qui peut aussi être créé de manière implicite). Le résultat du transfert d'une commande à la source de données et la réception de sa réponse est généralement représenté dans un objet **Recordset** ADO.</span><span class="sxs-lookup"><span data-stu-id="89ac5-p102">Several ADO objects can play a role in this operation. First you connect to the data source using an ADO **Connection** object (which at times will be created implicitly). Then you pass instructions to the data source about what you want to do using an ADO **Command** object (which also can be created implicitly). The result of passing a command to a data source and receiving its response usually will be represented in an ADO **Recordset** object.</span></span>

<span data-ttu-id="89ac5-110">Pour extraire les données, votre application doit être en communication avec une source de données, comme un SGBD, un stockage de fichiers ou un fichier texte délimité par des virgules.</span><span class="sxs-lookup"><span data-stu-id="89ac5-110">To get data, your application must be in communication with a data source, such as a DBMS, a file store, or a comma-delimited text file.</span></span> <span data-ttu-id="89ac5-111">Cette communication représente une *connexion* — l’environnement nécessaire pour l’échange de données.</span><span class="sxs-lookup"><span data-stu-id="89ac5-111">This communication represents a *connection* — the environment necessary for exchanging data.</span></span>

<span data-ttu-id="89ac5-p104">Le modèle d'objet ADO représente le concept d'une connexion avec l'objet **Connection**: la clé de voûte d'une grande partie de la fonctionnalité ADO. La finalité d'un objet **Connection** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="89ac5-p104">The ADO object model represents the concept of a connection with the **Connection** object — the foundation upon which much ADO functionality is built. The purpose of a **Connection** object is to:</span></span>

  - <span data-ttu-id="89ac5-114">Déterminer les informations qu'ADO doit communiquer aux sources de données et créer des sessions.</span><span class="sxs-lookup"><span data-stu-id="89ac5-114">Define the information ADO needs to communicate with data sources and create sessions.</span></span>

  - <span data-ttu-id="89ac5-115">Déterminer les capacités transactionnelles de la session.</span><span class="sxs-lookup"><span data-stu-id="89ac5-115">Define the transactional capabilities of the session.</span></span>

  - <span data-ttu-id="89ac5-116">Vous permettre de créer et d'exécuter des commandes sur la source de données.</span><span class="sxs-lookup"><span data-stu-id="89ac5-116">Allow you to create and execute commands against the data source.</span></span>

  - <span data-ttu-id="89ac5-p105">Fournir des informations sur la conception de la source de données sous-jacente sous la forme d'ensembles de lignes schématiques. Pour en savoir plus sur ces derniers, reportez-vous à la rubrique [OpenSchema, méthode](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="89ac5-p105">Provide information about the design of the underlying data source in the form of schema rowsets. For more information about schema rowsets, see [OpenSchema Method](openschema-method-ado.md).</span></span>

<span data-ttu-id="89ac5-119">Ce chapitre présente les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="89ac5-119">This chapter covers the following topics:</span></span>

  - [<span data-ttu-id="89ac5-120">Connexion</span><span class="sxs-lookup"><span data-stu-id="89ac5-120">Making a Connection</span></span>](making-a-connection.md)

  - [<span data-ttu-id="89ac5-121">Using the Connection Object Reference (ADO)</span><span class="sxs-lookup"><span data-stu-id="89ac5-121">Using the Connection Object Reference (ADO)</span></span>](using-the-connection-object-access.md)

  - [<span data-ttu-id="89ac5-122">Using the Command Object Reference (ADO)</span><span class="sxs-lookup"><span data-stu-id="89ac5-122">Using the Command Object Reference (ADO)</span></span>](using-the-command-object-access.md)

  - [<span data-ttu-id="89ac5-123">Adding Data to a Recordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="89ac5-123">Adding Data to a Recordset (ADO)</span></span>](adding-data-to-a-recordset.md)