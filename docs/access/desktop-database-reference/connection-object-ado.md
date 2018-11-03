---
title: Connection, objet (ADO)
TOCTitle: Connection object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7f35c2f76ec8cf2fd671f5ef9eefb42f8555237
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931385"
---
# <a name="connection-object-ado"></a><span data-ttu-id="fa113-102">Connection, objet (ADO)</span><span class="sxs-lookup"><span data-stu-id="fa113-102">Connection object (ADO)</span></span>

<span data-ttu-id="fa113-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa113-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa113-104">Représente une connexion ouverte à une source de données.</span><span class="sxs-lookup"><span data-stu-id="fa113-104">Represents an open connection to a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa113-105">Notes</span><span class="sxs-lookup"><span data-stu-id="fa113-105">Remarks</span></span>

<span data-ttu-id="fa113-p101">Un objet **Connection** représente une session unique avec une source de données. Dans le cas d'un système de base de données client/serveur, il peut être équivalent à une connexion réseau réelle au serveur. Selon les fonctionnalités prises en charge par le fournisseur, certaines collections, méthodes ou propriétés d'un objet **Connection** risquent de ne pas être disponibles.</span><span class="sxs-lookup"><span data-stu-id="fa113-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it may be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object may not be available.</span></span>

<span data-ttu-id="fa113-109">Les collections, les méthodes et les propriétés d'un objet **Connection** vous permettent d'effectuer diverses tâches :</span><span class="sxs-lookup"><span data-stu-id="fa113-109">With the collections, methods, and properties of a **Connection** object, you can do the following:</span></span>

  - <span data-ttu-id="fa113-p102">configurer la connexion avant de l'ouvrir avec les propriétés [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md) et [Mode](mode-property-ado.md) ( **ConnectionString** étant la propriété par défaut de l'objet **Connection** ) ;</span><span class="sxs-lookup"><span data-stu-id="fa113-p102">Configure the connection before opening it with the [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md), and [Mode](mode-property-ado.md) properties. **ConnectionString** is the default property of the **Connection** object.</span></span>

  - <span data-ttu-id="fa113-112">définir le client comme valeur de la propriété [CursorLocation](cursorlocation-property-ado.md) pour appeler [Service de curseur Microsoft pour OLE DB (composant du service ADO)](microsoft-cursor-service-for-ole-db-ado-service-component.md), qui prend en charge les mises à jour par lot ;</span><span class="sxs-lookup"><span data-stu-id="fa113-112">Set the [CursorLocation](cursorlocation-property-ado.md) property to client to invoke the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), which supports batch updates.</span></span>

  - <span data-ttu-id="fa113-113">définir la base de données par défaut de la connexion avec la propriété [DefaultDatabase](defaultdatabase-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="fa113-113">Set the default database for the connection with the [DefaultDatabase](defaultdatabase-property-ado.md) property.</span></span>

  - <span data-ttu-id="fa113-114">définir le niveau d'isolation des transactions ouvertes sur la connexion avec la propriété [IsolationLevel](isolationlevel-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="fa113-114">Set the level of isolation for the transactions opened on the connection with the [IsolationLevel](isolationlevel-property-ado.md) property.</span></span>

  - <span data-ttu-id="fa113-115">spécifier un fournisseur OLE DB avec la propriété [Provider](provider-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="fa113-115">Specify an OLE DB provider with the [Provider](provider-property-ado.md) property.</span></span>

  - <span data-ttu-id="fa113-116">établir (et ultérieurement rompre) la connexion physique à la source de données avec les méthodes [Open](open-method-ado-connection.md) et [Close](close-method-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="fa113-116">Establish, and later break, the physical connection to the data source with the [Open](open-method-ado-connection.md) and [Close](close-method-ado.md) methods.</span></span>

  - <span data-ttu-id="fa113-117">exécuter une commande sur la connexion avec la méthode [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) et configurer l'exécution avec la propriété [CommandTimeout](commandtimeout-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="fa113-117">Execute a command on the connection with the [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method and configure the execution with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="fa113-p103">[!REMARQUE] Pour exécuter une requête sans utiliser d'objet Command, passez une chaîne de requête à la méthode **Execute** d'un objet **Connection**. Toutefois, un objet [Command](command-object-ado.md) est nécessaire si vous voulez rendre persistant le texte de commande et l'exécuter de nouveau, ou utiliser des paramètres de requête.</span><span class="sxs-lookup"><span data-stu-id="fa113-p103">To execute a query without using a Command object, pass a query string to the **Execute** method of a **Connection** object. However, a [Command](command-object-ado.md) object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

  - <span data-ttu-id="fa113-120">gérer des transactions sur une connexion ouverte, notamment des transactions imbriquées si le fournisseur les prend en charge, avec les méthodes [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) et [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), ainsi qu'avec la propriété [Attributes](attributes-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="fa113-120">Manage transactions on the open connection, including nested transactions if the provider supports them, with the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), and [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) methods and the [Attributes](attributes-property-ado.md) property.</span></span>

  - <span data-ttu-id="fa113-121">examiner les erreurs renvoyées par la source de données à l'aide de la collection [Errors](errors-collection-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="fa113-121">Examine errors returned from the data source with the [Errors](errors-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="fa113-122">lire la version de l'implémentation ADO utilisée avec la propriété [Version](version-property-ado.md) ;</span><span class="sxs-lookup"><span data-stu-id="fa113-122">Read the version from the ADO implementation used with the [Version](version-property-ado.md) property.</span></span>

  - <span data-ttu-id="fa113-123">obtenir des informations de schéma sur votre base de données au moyen de la méthode [OpenSchema](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fa113-123">Obtain schema information about your database with the [OpenSchema](openschema-method-ado.md) method.</span></span>

<span data-ttu-id="fa113-124">Vous pouvez créer des objets **Connection** indépendamment de tout autre objet défini précédemment.</span><span class="sxs-lookup"><span data-stu-id="fa113-124">You can create **Connection** objects independently of any other previously defined object.</span></span>

<span data-ttu-id="fa113-125">Vous pouvez exécuter des commandes ou des procédures stockées comme si celles-ci étaient des méthodes natives de l'objet **Connection** (voir exemples ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="fa113-125">You can execute commands or stored procedures as if they were native methods on the **Connection** object, as illustrated below.</span></span>

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="fa113-126">Exécuter une commande comme une méthode native d'un objet Connection</span><span class="sxs-lookup"><span data-stu-id="fa113-126">Execute a command as a native method of a Connection object</span></span>

<span data-ttu-id="fa113-p104">Pour exécuter une commande, donnez-lui un nom à l'aide de la propriété **Name** de l'objet [Command](name-property-ado.md). Attribuez à la propriété **ActiveConnection** de l'objet **Command** le nom de la connexion. Émettez ensuite une instruction dans laquelle le nom de la commande est utilisé comme s'il s'agissait d'une méthode de l'objet **Connection**, suivie d'éventuels paramètres et ensuite d'un objet **Recordset** si des lignes sont renvoyées. Définissez les propriétés de **Recordset** de façon à personnaliser l'objet **Recordset** obtenu. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="fa113-p104">To execute a command, give the command a name using the **Command** object [Name](name-property-ado.md) property. Set the **Command** object's **ActiveConnection** property to the connection. Then issue a statement where the command name is used as if it were a method on the **Connection** object, followed by any parameters, then followed by a **Recordset** object if any rows are returned. Set the **Recordset** properties to customize the resulting **Recordset**. For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    Dim cmd As New ADODB.Command
    Dim rst As New ADODB.Recordset
    ...
    cnn.Open "..."
    cmd.Name = "yourCommandName"
    cmd.ActiveConnection = cnn
    ...
    'Your command name, any parameters, and an optional Recordset.
    cnn.yourCommandName "parameter", rst
```

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="fa113-132">Exécuter une procédure stockée comme une méthode native d'un objet Connection</span><span class="sxs-lookup"><span data-stu-id="fa113-132">Execute a stored procedure as a native method of a Connection object</span></span>

<span data-ttu-id="fa113-p105">Pour exécuter une procédure stockée, émettez une instruction dans laquelle le nom de la procédure stockée est utilisé comme s'il s'agissait d'une méthode de l'objet **Connection**, suivie d'éventuels paramètres. ADO détermine du mieux qu'il peut les types des paramètres. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="fa113-p105">To execute a stored procedure, issue a statement where the stored procedure name is used as if it were a method on the **Connection** object, followed by any parameters. ADO will make a "best guess" of parameter types. For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
