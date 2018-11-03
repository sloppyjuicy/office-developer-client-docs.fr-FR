---
title: Établissement d’une connexion
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0335c4bbc0d1240d6d4ca53ceacf47bf44fce67d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945886"
---
# <a name="making-a-connection"></a><span data-ttu-id="47561-102">Établissement d’une connexion</span><span class="sxs-lookup"><span data-stu-id="47561-102">Making a connection</span></span>

<span data-ttu-id="47561-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47561-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47561-p101">Pour vous connecter à une source de données, vous devez spécifier une *chaîne de connexion*, dont les paramètres peuvent être différents en fonction des fournisseurs et des sources de données. Pour en savoir plus, reportez-vous à la rubrique [Création de la chaîne de connexion](creating-the-connection-string.md).</span><span class="sxs-lookup"><span data-stu-id="47561-p101">To connect to a data source, you must specify a *connection string*, the parameters of which might differ for each provider and data source. For more information, see [Creating the Connection String](creating-the-connection-string.md).</span></span>

<span data-ttu-id="47561-p102">De manière générale, ADO ouvre une connexion à l'aide de la méthode **Connection** objet **Open**. La syntaxe de la méthode **Open** est illustrée ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="47561-p102">ADO most commonly opens a connection by using the **Connection** object **Open** method. The syntax for the **Open** method is shown here:</span></span>

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

<span data-ttu-id="47561-108">Vous pouvez également invoquer une technique de raccourci, **Recordset.Open**, pour ouvrir une connexion implicite et émettre une commande sur la connexion en une opération.</span><span class="sxs-lookup"><span data-stu-id="47561-108">Alternatively, you can invoke a shortcut technique, **Recordset.Open**, to open an implicit connection and issue a command over that connection in one operation.</span></span> <span data-ttu-id="47561-109">Cela en passant une chaîne de connexion valide comme l’argument *ActiveConnection* de la méthode **Open** .</span><span class="sxs-lookup"><span data-stu-id="47561-109">Do this by passing in a valid connection string as the *ActiveConnection* argument to the **Open** method.</span></span> <span data-ttu-id="47561-110">La syntaxe pour chaque méthode dans Visual Basic est présentée ci-après :</span><span class="sxs-lookup"><span data-stu-id="47561-110">Here is the syntax for each method in Visual Basic:</span></span>

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> <span data-ttu-id="47561-p104">[!REMARQUE] Quand utiliser un objet **Connection** plutôt qu'un raccourci **Recordset.Open** ? Utilisez un objet **Connection** lorsque vous envisagez d'ouvrir plusieurs **jeux d'enregistrements** ou lorsque vous exécutez des commandes multiples. Une connexion est toujours implicitement créée par ADO lorsque vous utilisez le raccourci **Recordset.Open**.</span><span class="sxs-lookup"><span data-stu-id="47561-p104">When should you use a **Connection** object vs. the **Recordset.Open** shortcut? Use the **Connection** object if you plan to open more than one **Recordset**, or when executing multiple commands. A connection is still created by ADO implicitly when you use the **Recordset.Open** shortcut.</span></span>


