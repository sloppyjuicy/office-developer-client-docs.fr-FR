---
title: En savoir plus sur la persistance des objets Recordset
TOCTitle: More about Recordset persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0b5888d5a616ad36812af93922cb085a5c8cbb7
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026077"
---
# <a name="more-about-recordset-persistence"></a><span data-ttu-id="7f9a4-102">En savoir plus sur la persistance des objets Recordset</span><span class="sxs-lookup"><span data-stu-id="7f9a4-102">More about Recordset persistence</span></span>

<span data-ttu-id="7f9a4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7f9a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f9a4-104">L'objet Recordset ADO prend en charge le stockage du contenu d'un objet **Recordset** dans un fichier à l'aide de la méthode [Save](save-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7f9a4-104">The ADO Recordset object supports storing a **Recordset** object's contents in a file using its [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="7f9a4-105">Le fichier stocké avec persistance peut-être exister sur un lecteur local, serveur réseau, ou en tant qu’URL sur un site Web.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-105">The persistently stored file may exist on a local drive, network server, or as a URL on a website.</span></span> <span data-ttu-id="7f9a4-106">Par la suite, le fichier peut être restauré soit avec la méthode **Open** de l'objet [Recordset](open-method-ado-recordset.md), soit avec la méthode [Execute](connection-object-ado.md) de l'objet [Connection](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection).</span><span class="sxs-lookup"><span data-stu-id="7f9a4-106">Later, the file can be restored with either the **Recordset** object's [Open](open-method-ado-recordset.md) method or the [Connection](connection-object-ado.md) object's [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method.</span></span>

<span data-ttu-id="7f9a4-107">En outre, la méthode [GetString](getstring-method-ado.md) convertit un objet **Recordset** dans un format où les lignes et les colonnes sont délimitées par des caractères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-107">In addition, the [GetString](getstring-method-ado.md) method converts a **Recordset** object to a form in which the columns and rows are delimited with characters you specify.</span></span>

<span data-ttu-id="7f9a4-p102">Pour rendre un objet **Recordset** persistant, commencez par le convertir dans un format qui lui permet d'être stocké dans un fichier. Les objets **Recordset** peuvent être stockés au format ADTG (Advanced Data TableGram) propriétaire ou au format XML (Extensible Markup Language) ouvert. Des exemples utilisant ADTG sont présentés ci-dessous. Pour plus d'informations sur la persistance XML, consultez [Persistance des enregistrements au format XML](persisting-records-in-xml-format.md).</span><span class="sxs-lookup"><span data-stu-id="7f9a4-p102">To persist a **Recordset**, begin by converting it to a form that can be stored in a file. **Recordset** objects can be stored in the proprietary Advanced Data TableGram (ADTG) format or the open Extensible Markup Language (XML) format. ADTG examples are shown below. For more information about XML persistence, see [Persisting Records in XML format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="7f9a4-112">Enregistrez les modifications en attente dans le fichier persisté.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-112">Save any pending changes in the persisted file.</span></span> <span data-ttu-id="7f9a4-113">Cela vous permet d’émettre une requête qui renvoie un objet **Recordset** , modifie le **jeu d’enregistrements**, enregistre ainsi que les modifications en attente, restaure l' **objet Recordset**et met à jour la source de données avec les modifications en attente.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-113">Doing this allows you to issue a query that returns a **Recordset** object, edits the **Recordset**, saves it and the pending changes, later restores the **Recordset**, and then updates the data source with the saved pending changes.</span></span>

<span data-ttu-id="7f9a4-114">Pour plus d'informations sur le stockage persistant des objets **Stream**, consultez [Flux et persistance](streams-and-persistence.md) au chapitre 10.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-114">For information about persistently storing **Stream** objects, see [Streams and Persistence](streams-and-persistence.md) in Chapter 10.</span></span>

<span data-ttu-id="7f9a4-115">Pour obtenir un exemple de persistance d'un objet **Recordset**, consultez [Scénario de persistance des objets Recordset XML](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="7f9a4-115">For an example of **Recordset** persistence, see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

## <a name="example"></a><span data-ttu-id="7f9a4-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="7f9a4-116">Example</span></span>

<span data-ttu-id="7f9a4-117">**Enregistrement d'un objet Recordset :**</span><span class="sxs-lookup"><span data-stu-id="7f9a4-117">**Save a Recordset:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

<span data-ttu-id="7f9a4-118">**Ouverture d'un fichier persistant avec Recordset.Open :**</span><span class="sxs-lookup"><span data-stu-id="7f9a4-118">**Open a persisted file with Recordset.Open:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

<span data-ttu-id="7f9a4-119">Si vous le souhaitez et si l'objet **Recordset** ne présente pas de connexion active, vous pouvez accepter toutes les valeurs par défaut et simplement coder ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="7f9a4-119">Optionally, if the **Recordset** does not have an active connection, you can accept all the defaults and simply code the following:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

<span data-ttu-id="7f9a4-120">**Ouverture d'un fichier persistant avec Connection.Execute :**</span><span class="sxs-lookup"><span data-stu-id="7f9a4-120">**Open a persisted file with Connection.Execute:**</span></span>

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

<span data-ttu-id="7f9a4-121">**Ouverture d'un fichier persistant avec RDS.DataControl :**</span><span class="sxs-lookup"><span data-stu-id="7f9a4-121">**Open a persisted file with RDS.DataControl:**</span></span>

<span data-ttu-id="7f9a4-122">Dans ce cas, la propriété **Server** n'est pas définie.</span><span class="sxs-lookup"><span data-stu-id="7f9a4-122">In this case, the **Server** property is not set.</span></span>

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

