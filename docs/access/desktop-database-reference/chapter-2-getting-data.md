---
title: 'Chapitre 2 : Obtention de données'
TOCTitle: 'Chapter 2: Getting data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f059e5dfe064442f10972fd36344e64f84fe7ea5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296443"
---
# <a name="chapter-2-getting-data"></a><span data-ttu-id="ec56c-102">Chapitre 2 : Obtention de données</span><span class="sxs-lookup"><span data-stu-id="ec56c-102">Chapter 2: Getting data</span></span>

<span data-ttu-id="ec56c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec56c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec56c-p101">Le chapitre précédent a présenté les quatre opérations primaires impliquées dans la création d'une application ADO : l'extraction des données, l'examen des données, la modification des données et la mise à jour des données. Ce chapitre va se pencher plus en détail sur les concepts relatifs à la première opération : l'extraction des données.</span><span class="sxs-lookup"><span data-stu-id="ec56c-p101">The preceding chapter introduced four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data. This chapter will focus on the details of the concepts relevant to the first operation: getting data.</span></span>

<span data-ttu-id="ec56c-p102">Plusieurs objets ADO peuvent jouer un rôle dans cette opération. Tout d'abord, vous vous connectez à la source de données à l'aide d'un objet **Connection** ADO (qui est parfois créé de manière implicite). Ensuite, vous transmettez vos instructions à la source de données à l'aide d'un objet **Command** ADO (qui peut aussi être créé de manière implicite). Le résultat du transfert d'une commande à la source de données et la réception de sa réponse est généralement représenté dans un objet **Recordset** ADO.</span><span class="sxs-lookup"><span data-stu-id="ec56c-p102">Several ADO objects can play a role in this operation. First you connect to the data source using an ADO **Connection** object (which at times will be created implicitly). Then you pass instructions to the data source about what you want to do using an ADO **Command** object (which also can be created implicitly). The result of passing a command to a data source and receiving its response usually will be represented in an ADO **Recordset** object.</span></span>

<span data-ttu-id="ec56c-p103">Pour extraire les données, votre application doit être en communication avec une source de données, comme un SGBD, un stockage de fichiers ou un fichier texte délimité par des virgules. Cette communication représente une *connexion* , l'environnement indispensable à tout échange de données.</span><span class="sxs-lookup"><span data-stu-id="ec56c-p103">To get data, your application must be in communication with a data source, such as a DBMS, a file store, or a comma-delimited text file. This communication represents a *connection* — the environment necessary for exchanging data.</span></span>

<span data-ttu-id="ec56c-p104">Le modèle d'objet ADO représente le concept d'une connexion avec l'objet **Connection**: la clé de voûte d'une grande partie de la fonctionnalité ADO. La finalité d'un objet **Connection** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="ec56c-p104">The ADO object model represents the concept of a connection with the **Connection** object — the foundation upon which much ADO functionality is built. The purpose of a **Connection** object is to:</span></span>

- <span data-ttu-id="ec56c-114">Déterminer les informations qu'ADO doit communiquer aux sources de données et créer des sessions.</span><span class="sxs-lookup"><span data-stu-id="ec56c-114">Define the information ADO needs to communicate with data sources and create sessions.</span></span>

- <span data-ttu-id="ec56c-115">Déterminer les capacités transactionnelles de la session.</span><span class="sxs-lookup"><span data-stu-id="ec56c-115">Define the transactional capabilities of the session.</span></span>

- <span data-ttu-id="ec56c-116">Vous permettre de créer et d'exécuter des commandes sur la source de données.</span><span class="sxs-lookup"><span data-stu-id="ec56c-116">Allow you to create and execute commands against the data source.</span></span>

- <span data-ttu-id="ec56c-p105">Fournir des informations sur la conception de la source de données sous-jacente sous la forme d'ensembles de lignes schématiques. Pour en savoir plus sur ces derniers, reportez-vous à la rubrique [OpenSchema, méthode](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ec56c-p105">Provide information about the design of the underlying data source in the form of schema rowsets. For more information about schema rowsets, see [OpenSchema Method](openschema-method-ado.md).</span></span>

<span data-ttu-id="ec56c-119">Ce chapitre présente les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ec56c-119">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="ec56c-120">Connexion</span><span class="sxs-lookup"><span data-stu-id="ec56c-120">Making a connection</span></span>](making-a-connection.md)
- [<span data-ttu-id="ec56c-121">Utilisation de la référence d’objet de connexion (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec56c-121">Using the connection object reference (ADO)</span></span>](using-the-connection-object-access.md)
- [<span data-ttu-id="ec56c-122">Utilisation de la référence d’objet de commande (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec56c-122">Using the command object reference (ADO)</span></span>](using-the-command-object-access.md)
- [<span data-ttu-id="ec56c-123">Ajout de données à un recordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec56c-123">Adding data to a Recordset (ADO)</span></span>](adding-data-to-a-recordset.md)
