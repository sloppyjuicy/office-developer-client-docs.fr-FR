---
title: Resync Command, propriété dynamique (ADO)
TOCTitle: Resync Command Property--Dynamic (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d9133f37b236cfa876a5d6ae8642f25f919f2cb
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602803"
---
# <a name="resync-command-property--dynamic-ado"></a>Resync Command, propriété dynamique (ADO)

**S’applique à**: Access 2013 | Office 2013

Spécifie une chaîne de commande fournie par l'utilisateur, que la méthode [Resync](resync-method-ado.md) émet pour actualiser les données de la table nommée dans la propriété dynamique [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **String** qui représente une chaîne de commande.

## <a name="remarks"></a>Notes

L'objet [Recordset](recordset-object-ado.md) est le résultat d'une opération JOIN exécutée sur plusieurs tables de base. Les lignes affectées dépendent du paramètre *AffectRecords* de la méthode [Resync](resync-method-ado.md) . La méthode **Resync** est exécutée si les propriétés [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) et **Resync Command** ne sont pas définies.

La chaîne de commande de la propriété **Resync Command** est une commande paramétrée ou une procédure stockée, qui identifie de manière unique la ligne actualisée, et renvoie une ligne unique avec un nombre et un ordre de colonnes identiques à celles de la ligne à actualiser. La chaîne de commande doit contenir un paramètre pour chaque colonne de clé primaire dans la propriété **Unique Table** sans quoi une erreur d'exécution est renvoyée. Les paramètres sont remplis automatiquement avec les valeurs de clé primaire dans la ligne à actualiser.

Voici deux exemples basés sur le langage SQL :

1.  L'objet **Recordset** est défini par une commande :

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    La propriété **Resync Command** est définie comme suit :

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    La propriété **Unique Table** a la valeur *Orders* et sa clé primaire, *OrderID*, est paramétrée. L'instruction Select secondaire permet de garantir, par programme, le retour du même nombre de colonnes dans un ordre identique à celles renvoyées par la commande d'origine.

2. L'objet **Recordset** est défini par une procédure stockée :

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    La méthode **Resync** doit exécuter la procédure stockée suivante :

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    La propriété **Resync Command** est définie comme suit :

    `"{call CustordersResync (?)}"`

Une fois encore, la propriété **Unique Table** a la valeur *Orders* et sa clé primaire, *OrderID*, est paramétrée.

La propriété **Resync Command** est une propriété dynamique ajoutée à la collection **Properties** de l'objet [Recordset](properties-collection-ado.md) lorsque la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**.

