---
title: Command, objet (ADO)
TOCTitle: Command Object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 48f30471dd5df224e8fe01538dc02d85ded54d6a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470088"
---
# <a name="command-object-ado"></a><span data-ttu-id="d0ad9-102">Command, objet (ADO)</span><span class="sxs-lookup"><span data-stu-id="d0ad9-102">Command Object (ADO)</span></span>


<span data-ttu-id="d0ad9-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0ad9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d0ad9-104">Définit une commande spécifique que vous avez l'intention d'exécuter sur une source de données.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-104">Defines a specific command that you intend to execute against a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0ad9-105">Notes</span><span class="sxs-lookup"><span data-stu-id="d0ad9-105">Remarks</span></span>

<span data-ttu-id="d0ad9-p101">Utilisez un objet **Command** pour interroger une base de données et renvoyer des enregistrements dans un objet [Recordset](recordset-object-ado.md), pour exécuter une opération en bloc ou pour manipuler la structure d'une base de données. Selon les fonctionnalités proposées par le fournisseur, certaines collections, méthodes ou propriétés **Command** risquent de générer une erreur lorsqu'elles sont référencées.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-p101">Use a **Command** object to query a database and return records in a [Recordset](recordset-object-ado.md) object, to execute a bulk operation, or to manipulate the structure of a database. Depending on the functionality of the provider, some **Command** collections, methods, or properties may generate an error when referenced.</span></span>

<span data-ttu-id="d0ad9-108">Les collections, les méthodes et les propriétés d'un objet **Command** vous permettent d'effectuer diverses tâches :</span><span class="sxs-lookup"><span data-stu-id="d0ad9-108">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="d0ad9-109">définir le texte exécutable de la commande (par exemple, une instruction SQL) avec la propriété [CommandText](commandtext-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="d0ad9-109">Define the executable text of the command (for example, an SQL statement) with the [CommandText](commandtext-property-ado.md) property.</span></span>

  - <span data-ttu-id="d0ad9-110">Définir des requêtes paramétrées ou des arguments de procédure stockée à l'aide des objets [Parameter](parameter-object-ado.md) et de la collection [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d0ad9-110">Define parameterized queries or stored-procedure arguments with [Parameter](parameter-object-ado.md) objects and the [Parameters](parameters-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="d0ad9-111">exécuter une commande et renvoyer le cas échéant un objet **Recordset** avec la méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) ;</span><span class="sxs-lookup"><span data-stu-id="d0ad9-111">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>

  - <span data-ttu-id="d0ad9-112">spécifier le type de commande avec la propriété [CommandType](commandtype-property-ado.md) avant exécution afin d'optimiser les performances ;</span><span class="sxs-lookup"><span data-stu-id="d0ad9-112">Specify the type of command with the [CommandType](commandtype-property-ado.md) property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="d0ad9-113">vérifier que le fournisseur enregistre une version préparée (compilée) de la commande avant exécution avec la propriété [Prepared](prepared-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="d0ad9-113">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the [Prepared](prepared-property-ado.md) property.</span></span>

  - <span data-ttu-id="d0ad9-114">définir le nombre de secondes pendant lesquelles un fournisseur attendra qu'une commande s'exécute avec la propriété [CommandTimeout](commandtimeout-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="d0ad9-114">Set the number of seconds that a provider will wait for a command to execute with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>

  - <span data-ttu-id="d0ad9-115">associer une connexion ouverte à un objet **Command** en définissant sa propriété [ActiveConnection](activeconnection-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="d0ad9-115">Associate an open connection with a **Command** object by setting its [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="d0ad9-116">définir la propriété [Name](name-property-ado.md) pour identifier l'objet **Command** en tant que méthode pour l'objet [Connection](connection-object-ado.md) associé ;</span><span class="sxs-lookup"><span data-stu-id="d0ad9-116">Set the [Name](name-property-ado.md) property to identify the **Command** object as a method on the associated [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="d0ad9-117">passer un objet **Command** à la propriété [Source](source-property-ado-recordset.md) d'un objet **Recordset** afin d'obtenir des données ;</span><span class="sxs-lookup"><span data-stu-id="d0ad9-117">Pass a **Command** object to the [Source](source-property-ado-recordset.md) property of a **Recordset** in order to obtain data.</span></span>

  - <span data-ttu-id="d0ad9-118">accéder aux attributs spécifiques du fournisseur avec la collection [Properties](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d0ad9-118">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d0ad9-p102">[!REMARQUE] Pour exécuter une requête sans utiliser d'objet <STRONG>Command</STRONG>, passez une chaîne de requête à la méthode <A href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</A> d'un objet <STRONG>Connection</STRONG> ou à la méthode <A href="open-method-ado-recordset.md">Open</A> d'un objet <STRONG>Recordset</STRONG>. Toutefois, un objet <STRONG>Command</STRONG> est nécessaire si vous voulez rendre persistant le texte de commande et l'exécuter de nouveau, ou utiliser des paramètres de requête.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-p102">To execute a query without using a <STRONG>Command</STRONG> object, pass a query string to the <A href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute</A> method of a <STRONG>Connection</STRONG> object or to the <A href="open-method-ado-recordset.md">Open</A> method of a <STRONG>Recordset</STRONG> object. However, a <STRONG>Command</STRONG> object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span></P>



<span data-ttu-id="d0ad9-p103">Pour créer un objet **Command** indépendamment d'un objet **Connection** déjà défini, définissez sa propriété **ActiveConnection** sur une chaîne de connexion valide. ADO crée tout de même un objet **Connection**, mais il ne l'affecte pas à une variable objet. Toutefois, si vous associez plusieurs objets **Command** à la même connexion, vous devez créer et ouvrir explicitement un objet **Connection**; l'objet **Connection** est ainsi affecté à une variable objet. Si vous ne définissez pas la propriété **ActiveConnection** de l'objet **Connection** avec cette variable objet, ADO crée un nouvel objet **Connection** pour chaque objet **Command**, même si vous utilisez la même chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-p103">To create a **Command** object independently of a previously defined **Connection** object, set its **ActiveConnection** property to a valid connection string. ADO still creates a **Connection** object, but it doesn't assign that object to an object variable. However, if you are associating multiple **Command** objects with the same connection, you should explicitly create and open a **Connection** object; this assigns the **Connection** object to an object variable. If you do not set the **Command** object's **ActiveConnection** property to this object variable, ADO creates a new **Connection** object for each **Command** object, even if you use the same connection string.</span></span>

<span data-ttu-id="d0ad9-p104">Pour exécuter un objet **Command**, il vous suffit de l'appeler à l'aide de sa propriété [Name](name-property-ado.md) sur l'objet **Connection** associé. La propriété **ActiveConnection** de **Command** doit être définie sur l'objet **Connection**. Si **Command** possède des paramètres, passez ses valeurs en tant qu'arguments à la méthode.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-p104">To execute a **Command**, simply call it by its [Name](name-property-ado.md) property on the associated **Connection** object. The **Command** must have its **ActiveConnection** property set to the **Connection** object. If the **Command** has parameters, pass their values as arguments to the method.</span></span>

<span data-ttu-id="d0ad9-p105">Si deux objets **Command** ou plus sont exécutés sur la même connexion et que l'un d'eux\*\*\*\* est une procédure stockée sans paramètres de sortie, une erreur se produit. Pour exécuter chaque objet **Command**, utilisez des connexions distinctes ou déconnectez tous les autres objets **Command**.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-p105">If two or more **Command** objects are executed on the same connection and either **Command** object is a stored procedure with output parameters, an error occurs. To execute each **Command** object, use separate connections or disconnect all other **Command** objects from the connection.</span></span>

<span data-ttu-id="d0ad9-p106">La collection **Parameters** est le membre par défaut de l'objet **Command**. Les deux instructions suivantes sont donc équivalentes.</span><span class="sxs-lookup"><span data-stu-id="d0ad9-p106">The **Parameters** collection is the default member of the **Command** object. As a result, the following two code statements are equivalent.</span></span>

