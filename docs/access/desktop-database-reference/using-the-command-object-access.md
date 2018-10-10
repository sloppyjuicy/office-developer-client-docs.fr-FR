---
title: Using the Command Object (Access)
TOCTitle: Using the Command Object
ms:assetid: dab6f0dd-1efa-3a5c-b192-c6d6afcaabfb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250102(v=office.15)
ms:contentKeyID: 48548088
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36d7bf1b39186eca841e417473e31e2bfd3a2dfc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469549"
---
# <a name="using-the-command-object-access"></a><span data-ttu-id="c7664-102">Using the Command Object (Access)</span><span class="sxs-lookup"><span data-stu-id="c7664-102">Using the Command Object (Access)</span></span>


<span data-ttu-id="c7664-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7664-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c7664-p101">Une fois connecté à une source de données, vous devez y exécuter des requêtes pour obtenir des jeux de résultats. ADO encapsule ce type de fonctionnalité de commande dans l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="c7664-p101">After connecting to a data source, you need to execute requests against it to obtain result sets. ADO encapsulates this type of command functionality in the **Command** object.</span></span>

<span data-ttu-id="c7664-p102">Vous pouvez utiliser l'objet **Command** pour demander au fournisseur n'importe quel type d'opération, à condition que ce dernier puisse interpréter correctement la chaîne de commande. Une des opérations courantes pour les fournisseurs de données est l'interrogation d'une base de données et le renvoi des enregistrements correspondants dans un objet **Recordset**. Les objets **Recordset** seront présentés plus loin dans ce chapitre et dans d'autres chapitres. Considérons-les pour l'instant comme des outils permettant de stocker et d'afficher des jeux de résultats. Comme pour un certain nombre d'objets ADO, selon les fonctionnalités offertes par le fournisseur, la référence à certaines collections, méthodes ou propriétés de l'objet **Command** peut générer des erreurs.</span><span class="sxs-lookup"><span data-stu-id="c7664-p102">You can use the **Command** object to request any type of operation from the provider, assuming that the provider can interpret the command string properly. A common operation for data providers is to query a database and return records in a **Recordset** object. **Recordset**s will be discussed later in this and other chapters; for now, think of them as tools to hold and view result sets. As with many ADO objects, depending on the functionality of the provider, some **Command** object collections, methods, or properties might generate errors when referenced.</span></span>

<span data-ttu-id="c7664-p103">Il n'est pas toujours nécessaire de créer un objet **Command** pour exécuter une commande sur une source de données. Vous pouvez utiliser la méthode **Execute** sur l'objet **Connection**, ou la méthode **Open** sur l'objet **Recordset**. Toutefois, vous devez impérativement utiliser un objet **Command** si vous devez réutiliser une commande dans votre code ou si vous devez transmettre des informations de paramétrage avec votre commande. Ces scénarios sont présentés en détail dans une autre section du présent chapitre.</span><span class="sxs-lookup"><span data-stu-id="c7664-p103">It is not always necessary to create a **Command** object to execute a command against a data source. You can use the **Execute** method on the **Connection** object or the **Open** method on the **Recordset** object. However, you should use a **Command** object if you need to reuse a command in your code or if you need to pass detailed parameter information with your command. These scenarios are covered in more detail later in this chapter.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c7664-p104">Certains objets <STRONG>Command</STRONG> peuvent renvoyer un jeu de résultats sous la forme d’un flux binaire ou d’un objet <STRONG>Record</STRONG> unique, plutôt que sous forme d’un objet <STRONG>Recordset</STRONG>, si le fournisseur le prend en charge. En outre, certains objets <STRONG>Command</STRONG> ne sont pas conçus pour renvoyer de jeu de résultats (par exemple, une requête SQL Update). Ce chapitre présente le scénario le plus courant, c’est-à-dire l’exécution d’objets <STRONG>Command</STRONG> renvoyant ses résultats dans un objet <STRONG>Recordset</STRONG>. Pour plus d’informations sur le renvoi de résultats dans les objets <STRONG>Recordset</STRONG> ou <STRONG>Stream</STRONG>,  consultez le <A href="chapter-10-records-and-streams.md">Chapitre 10 : Enregistrements et flux</A>.</span><span class="sxs-lookup"><span data-stu-id="c7664-p104">Certain <STRONG>Command</STRONG>s can return a result set as a binary stream or as a single <STRONG>Record</STRONG> rather than as a <STRONG>Recordset</STRONG>, if this is supported by the provider. Also, some <STRONG>Command</STRONG>s are not intended to return any result set at all (for example, a SQL Update query). This chapter will cover the most typical scenario, however: executing <STRONG>Command</STRONG>s that return results into a <STRONG>Recordset</STRONG> object. For more information about returning results into <STRONG>Record</STRONG>s or <STRONG>Stream</STRONG>s, see <A href="chapter-10-records-and-streams.md">Chapter 10: Records and Streams</A>.</span></span></P>


