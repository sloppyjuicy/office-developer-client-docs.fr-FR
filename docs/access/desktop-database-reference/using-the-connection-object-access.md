---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc797bd6caf95c731d454ed4a81329b8c2600470
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870484"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="6600c-102">Using the Connection Object (Access)</span><span class="sxs-lookup"><span data-stu-id="6600c-102">Using the Connection Object (Access)</span></span>


<span data-ttu-id="6600c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6600c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6600c-p101">Un objet **Connection** représente une session unique associée à une source de données. Dans le cas d'un système de base de données client/serveur, il peut être apparenté à une connexion réseau au serveur. Selon les fonctionnalités prises en charge par le fournisseur, il est possible que certaines collections, méthodes ou propriétés d'un objet **Connection** ne soient pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="6600c-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it can be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="6600c-107">Avant d'ouvrir un objet **Connection**, vous devez définir certaines informations concernant la source de données et le type de connexion.</span><span class="sxs-lookup"><span data-stu-id="6600c-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="6600c-108">Le paramètre *ConnectionString* de la méthode **Open** de l’objet **Connection** , ou la propriété **ConnectionString** de l’objet **Connection** , contient généralement la plupart de ces informations.</span><span class="sxs-lookup"><span data-stu-id="6600c-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="6600c-109">Une chaîne de connexion est une chaîne de caractères qui définit un nombre variable d'arguments.</span><span class="sxs-lookup"><span data-stu-id="6600c-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="6600c-110">Les arguments , qu'ils soient requis par ADO ou spécifiques au fournisseur, contiennent les informations dont l'objet **Connection** a besoin pour établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="6600c-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="6600c-111">Les arguments constituant le paramètre *ConnectionString* sont séparés par des points-virgules ( ;).</span><span class="sxs-lookup"><span data-stu-id="6600c-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>

> [!NOTE]
> <span data-ttu-id="6600c-p103">Vous pouvez également spécifier un fichier DSN (Data Source Name) ODBC ou UDL (Data Link) dans une chaîne de connexion. Pour plus d'informations sur les fichiers DSN, consultez la section Data Sources dans la première partie du manuel *ODBC Programmer's Reference* (en anglais). Pour plus d'informations sur les fichiers UDL, consultez la section Data Link API Overview du manuel *OLE DB Programmer's Reference* (en anglais).</span><span class="sxs-lookup"><span data-stu-id="6600c-p103">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string. For more information about DSNs, see Data Sources in Part 1 of the *ODBC Programmer's Reference*. For more information about UDLs, see Data Link API Overview in the *OLE DB Programmer's Reference*.</span></span>

<span data-ttu-id="6600c-115">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="6600c-115">This section includes the following topics:</span></span>

- [<span data-ttu-id="6600c-116">Création de la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="6600c-116">Creating the Connection String</span></span>](creating-the-connection-string.md)

- [<span data-ttu-id="6600c-117">Contrôle des transactions</span><span class="sxs-lookup"><span data-stu-id="6600c-117">Controlling Transactions</span></span>](controlling-transactions.md)
