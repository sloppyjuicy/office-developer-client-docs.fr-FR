---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd3e691258fe5950f40c36a1efcaed8e79810c7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470284"
---
# <a name="using-the-connection-object-access"></a><span data-ttu-id="b5405-102">Using the Connection Object (Access)</span><span class="sxs-lookup"><span data-stu-id="b5405-102">Using the Connection Object (Access)</span></span>


<span data-ttu-id="b5405-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5405-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b5405-p101">Un objet **Connection** représente une session unique associée à une source de données. Dans le cas d'un système de base de données client/serveur, il peut être apparenté à une connexion réseau au serveur. Selon les fonctionnalités prises en charge par le fournisseur, il est possible que certaines collections, méthodes ou propriétés d'un objet **Connection** ne soient pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="b5405-p101">A **Connection** object represents a unique session with a data source. In the case of a client/server database system, it can be equivalent to an actual network connection to the server. Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object might not be available.</span></span>

<span data-ttu-id="b5405-107">Avant d'ouvrir un objet **Connection**, vous devez définir certaines informations concernant la source de données et le type de connexion.</span><span class="sxs-lookup"><span data-stu-id="b5405-107">Before opening a **Connection** object, you must define certain information about the data source and type of connection.</span></span> <span data-ttu-id="b5405-108">Le paramètre *ConnectionString* de la méthode **Open** de l’objet **Connection** , ou la propriété **ConnectionString** de l’objet **Connection** , contient généralement la plupart de ces informations.</span><span class="sxs-lookup"><span data-stu-id="b5405-108">The *ConnectionString* parameter of the **Connection** object **Open** method — or the **ConnectionString** property on the **Connection** object — usually contains most of this information.</span></span> <span data-ttu-id="b5405-109">Une chaîne de connexion est une chaîne de caractères qui définit un nombre variable d'arguments.</span><span class="sxs-lookup"><span data-stu-id="b5405-109">A connection string is a string of characters that defines a variable number of arguments.</span></span> <span data-ttu-id="b5405-110">Les arguments , qu'ils soient requis par ADO ou spécifiques au fournisseur, contiennent les informations dont l'objet **Connection** a besoin pour établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="b5405-110">The arguments — some required by ADO, but others provider-specific — contain information that the **Connection** object must have to carry out its work.</span></span> <span data-ttu-id="b5405-111">Les arguments constituant le paramètre *ConnectionString* sont séparés par des points-virgules ( ;).</span><span class="sxs-lookup"><span data-stu-id="b5405-111">The arguments that make up the *ConnectionString* parameter are separated with semicolons (;).</span></span>


> [!NOTE]
> <P><span data-ttu-id="b5405-p103">Vous pouvez également spécifier un fichier DSN (Data Source Name) ODBC ou UDL (Data Link) dans une chaîne de connexion. Pour plus d'informations sur les fichiers DSN, consultez la section Data Sources dans la première partie du manuel <EM>ODBC Programmer's Reference</EM> (en anglais). Pour plus d'informations sur les fichiers UDL, consultez la section Data Link API Overview du manuel <EM>OLE DB Programmer's Reference</EM> (en anglais).</span><span class="sxs-lookup"><span data-stu-id="b5405-p103">You can also specify an ODBC Data Source Name (DSN) or a Data Link (UDL) file in a connection string. For more information about DSNs, see Data Sources in Part 1 of the <EM>ODBC Programmer's Reference</EM>. For more information about UDLs, see Data Link API Overview in the <EM>OLE DB Programmer's Reference</EM>.</span></span></P>


