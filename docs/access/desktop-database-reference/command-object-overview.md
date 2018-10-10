---
title: Vue d'ensemble de l'objet Command
TOCTitle: Command Object Overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1e6cd3b2ebea67fac7cef7e556038490b3eb9b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472244"
---
# <a name="command-object-overview"></a><span data-ttu-id="1b4a1-102">Vue d'ensemble de l'objet Command</span><span class="sxs-lookup"><span data-stu-id="1b4a1-102">Command Object Overview</span></span>


<span data-ttu-id="1b4a1-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b4a1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1b4a1-104">Grâce aux collections, aux méthodes et aux propriétés d'un objet **Command**, vous pouvez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1b4a1-104">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="1b4a1-105">Définir le texte exécutable de la commande (par exemple, une instruction SQL ou une procédure stockée) en utilisant la propriété **CommandText**.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-105">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the **CommandText** property.</span></span>

  - <span data-ttu-id="1b4a1-106">Définir des requêtes paramétrées ou des arguments de procédure stockée à l'aide des objets **Parameter** et de la collection **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-106">Define parameterized queries or stored procedure arguments by using **Parameter** objects and the **Parameters** collection.</span></span>

  - <span data-ttu-id="1b4a1-107">Exécuter une commande et retourner un objet **Recordset**, le cas échéant, en utilisant la méthode **Execute**.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-107">Execute a command and return a **Recordset** object, if appropriate, by using the **Execute** method.</span></span>

  - <span data-ttu-id="1b4a1-108">Spécifier le type de commande en utilisant la propriété **CommandType** avant l'exécution afin d'optimiser les performances.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-108">Specify the type of command by using the **CommandType** property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="1b4a1-109">Vérifier si le fournisseur enregistre une version préparée (ou compilée) de la commande avant l'exécution en utilisant la propriété **Prepared**.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-109">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the **Prepared** property.</span></span>

  - <span data-ttu-id="1b4a1-110">Définir le nombre de secondes d'attente d'un fournisseur pour l'exécution d'une commande à l'aide de la propriété **CommandTimeout**.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-110">Set the number of seconds that a provider will wait for a command to execute by using the **CommandTimeout** property.</span></span>

  - <span data-ttu-id="1b4a1-111">Associer une connexion ouverte à un objet **Command** en définissant sa propriété **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-111">Associate an open connection with a **Command** object by setting its **ActiveConnection** property.</span></span>

  - <span data-ttu-id="1b4a1-112">définir la propriété **Name** pour identifier l'objet **Command** en tant que méthode pour l'objet **Connection** associé ;</span><span class="sxs-lookup"><span data-stu-id="1b4a1-112">Set the **Name** property to identify the **Command** object as a method on the associated **Connection** object.</span></span>

  - <span data-ttu-id="1b4a1-113">Passer un objet **Command** à la propriété **Source** d'un objet **Recordset** pour obtenir des données.</span><span class="sxs-lookup"><span data-stu-id="1b4a1-113">Pass a **Command** object to the **Source** property of a **Recordset** in order to obtain data.</span></span>

