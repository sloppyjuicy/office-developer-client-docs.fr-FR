---
title: Modèle de programmation RDS avec des objets
TOCTitle: RDS Programming Model with Objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6d28373e5d241ae9e87357187894924f27ba78c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873802"
---
# <a name="rds-programming-model-with-objects"></a><span data-ttu-id="1b1a1-102">Modèle de programmation RDS avec des objets</span><span class="sxs-lookup"><span data-stu-id="1b1a1-102">RDS Programming Model with Objects</span></span>


<span data-ttu-id="1b1a1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b1a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b1a1-p101">L'objectif de RDS est de pouvoir accéder aux sources de données et de les mettre à jour via un service intermédiaire, tel qu'IIS. Le modèle de programmation spécifie la séquence d'activités nécessaires à la réalisation de cet objectif. Le modèle objet spécifie les objets dont les méthodes et les propriétés ont une incidence sur le modèle de programmation.</span><span class="sxs-lookup"><span data-stu-id="1b1a1-p101">The goal of RDS is to gain access to and update data sources through an intermediary such as IIS. The programming model specifies the sequence of activities necessary to accomplish this goal. The object model specifies the objects whose methods and properties affect the programming model.</span></span>

<span data-ttu-id="1b1a1-107">RDS offre la possibilité d'exécuter les séquences d'actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="1b1a1-107">RDS provides the means to perform the following sequence of actions:</span></span>

  - <span data-ttu-id="1b1a1-108">Spécifier le programme à appeler sur le serveur et obtenir un moyen (proxy) d'y faire référence à partir du client ([RDS.DataSpace](dataspace-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="1b1a1-108">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client ([RDS.DataSpace](dataspace-object-rds.md)).</span></span>

  - <span data-ttu-id="1b1a1-p102">Appeler le programme serveur et passer les paramètres au programme serveur qui identifie la source de données et la commande à émettre (proxy ou [RDS.DataControl](datacontrol-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="1b1a1-p102">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue (proxy or [RDS.DataControl](datacontrol-object-rds.md)).</span></span>

  - <span data-ttu-id="1b1a1-p103">Le programme serveur obtient un objet [Recordset](recordset-object-ado.md) de la source de données, en général à l’aide d’ADO. Le cas échéant, l’objet **Recordset** est traité sur le serveur ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span><span class="sxs-lookup"><span data-stu-id="1b1a1-p103">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).</span></span>

  - <span data-ttu-id="1b1a1-113">Le programme serveur retourne l'objet **Recordset** final à l'application cliente (proxy).</span><span class="sxs-lookup"><span data-stu-id="1b1a1-113">The server program returns the final **Recordset** object to the client application (proxy).</span></span>

  - <span data-ttu-id="1b1a1-114">Sur le client, l'objet **Recordset** est présenté sous une forme facilement utilisable par les contrôles visuels (contrôle visuel et **RDS.DataControl**).</span><span class="sxs-lookup"><span data-stu-id="1b1a1-114">On the client, the **Recordset** object is put into a form that can be easily used by visual controls (visual control and **RDS.DataControl**).</span></span>

  - <span data-ttu-id="1b1a1-115">Les modifications apportées à l'objet **Recordset** sont renvoyées au serveur et utilisées pour mettre à jour la source de données (**RDS.DataControl** ou **RDSServer.DataFactory**).</span><span class="sxs-lookup"><span data-stu-id="1b1a1-115">Changes to the **Recordset** object are sent back to the server and used to update the data source (**RDS.DataControl** or **RDSServer.DataFactory**).</span></span>

