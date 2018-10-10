---
title: Resync Command, propriété dynamique (ADO)
TOCTitle: Resync Command Property--Dynamic (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8fc64a51044f219d4daae44a9c684506cd7bd5c6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470010"
---
# <a name="resync-command-property--dynamic-ado"></a><span data-ttu-id="65761-102">Resync Command, propriété dynamique (ADO)</span><span class="sxs-lookup"><span data-stu-id="65761-102">Resync Command Property--Dynamic (ADO)</span></span>

<span data-ttu-id="65761-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="65761-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="65761-104">Spécifie une chaîne de commande fournie par l'utilisateur, que la méthode [Resync](resync-method-ado.md) émet pour actualiser les données de la table nommée dans la propriété dynamique [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="65761-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="65761-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="65761-105">Settings and Return Values</span></span>

<span data-ttu-id="65761-106">Définit ou renvoie une valeur de type **String** qui représente une chaîne de commande.</span><span class="sxs-lookup"><span data-stu-id="65761-106">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="65761-107">Notes</span><span class="sxs-lookup"><span data-stu-id="65761-107">Remarks</span></span>

<span data-ttu-id="65761-108">L'objet [Recordset](recordset-object-ado.md) est le résultat d'une opération JOIN exécutée sur plusieurs tables de base.</span><span class="sxs-lookup"><span data-stu-id="65761-108">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables.</span></span> <span data-ttu-id="65761-109">Les lignes affectées dépendent du paramètre *AffectRecords* de la méthode [Resync](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="65761-109">The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method.</span></span> <span data-ttu-id="65761-110">La méthode **Resync** est exécutée si les propriétés [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) et **Resync Command** ne sont pas définies.</span><span class="sxs-lookup"><span data-stu-id="65761-110">The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="65761-p102">La chaîne de commande de la propriété **Resync Command** est une commande paramétrée ou une procédure stockée, qui identifie de manière unique la ligne actualisée, et renvoie une ligne unique avec un nombre et un ordre de colonnes identiques à celles de la ligne à actualiser. La chaîne de commande doit contenir un paramètre pour chaque colonne de clé primaire dans la propriété **Unique Table** sans quoi une erreur d'exécution est renvoyée. Les paramètres sont remplis automatiquement avec les valeurs de clé primaire dans la ligne à actualiser.</span><span class="sxs-lookup"><span data-stu-id="65761-p102">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed. The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned. The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="65761-114">Voici deux exemples basés sur le langage SQL :</span><span class="sxs-lookup"><span data-stu-id="65761-114">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="65761-115">L'objet **Recordset** est défini par une commande :</span><span class="sxs-lookup"><span data-stu-id="65761-115">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="65761-116">La propriété **Resync Command** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="65761-116">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="65761-p103">La propriété **Unique Table** a la valeur *Orders* et sa clé primaire, *OrderID*, est paramétrée. L'instruction Select secondaire permet de garantir, par programme, le retour du même nombre de colonnes dans un ordre identique à celles renvoyées par la commande d'origine.</span><span class="sxs-lookup"><span data-stu-id="65761-p103">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized. The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="65761-119">L'objet **Recordset** est défini par une procédure stockée :</span><span class="sxs-lookup"><span data-stu-id="65761-119">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="65761-120">La méthode **Resync** doit exécuter la procédure stockée suivante :</span><span class="sxs-lookup"><span data-stu-id="65761-120">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="65761-121">La propriété **Resync Command** est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="65761-121">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="65761-122">Une fois encore, la propriété **Unique Table** a la valeur *Orders* et sa clé primaire, *OrderID*, est paramétrée.</span><span class="sxs-lookup"><span data-stu-id="65761-122">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="65761-123">La propriété **Resync Command** est une propriété dynamique ajoutée à la collection **Properties** de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="65761-123">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

