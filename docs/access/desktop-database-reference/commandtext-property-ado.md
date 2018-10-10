---
title: CommandText, propriété (ADO)
TOCTitle: CommandText Property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9000f069c7669872c686c013520f886d16e3619b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469134"
---
# <a name="commandtext-property-ado"></a><span data-ttu-id="0b4cf-102">CommandText, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="0b4cf-102">CommandText Property (ADO)</span></span>


<span data-ttu-id="0b4cf-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b4cf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0b4cf-104">Indique le texte d'une commande à émettre sur un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-104">Indicates the text of a command to be issued against a provider.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="0b4cf-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="0b4cf-105">Settings and Return Values</span></span>

<span data-ttu-id="0b4cf-p101">Définit ou renvoie une valeur de type **String** qui contient une commande de fournisseur, comme une instruction SQL, un nom de table, une URL relative ou un appel de procédure stockée. La valeur par défaut est "" (chaîne de longueur zéro).</span><span class="sxs-lookup"><span data-stu-id="0b4cf-p101">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call. Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b4cf-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0b4cf-108">Remarks</span></span>

<span data-ttu-id="0b4cf-p102">Utilisez la propriété **CommandText** pour définir ou renvoyer le texte d'une commande représentée par un objet [Command](command-object-ado.md). En général, il s'agit d'une instruction SQL, mais il peut également s'agir d'un autre type d'instruction de commande reconnu par le fournisseur, comme un appel de procédure stockée. Le langage, ou la version, utilisé pour une instruction SQL doit être pris en charge par le processeur de requêtes du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-p102">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object. Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call. An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="0b4cf-112">Si la propriété [Prepared](prepared-property-ado.md) de l'objet **Command** a la valeur **True** et que l'objet **Command** est lié à une connexion ouverte lorsque vous définissez la propriété **CommandText**, ADO prépare la requête (c'est-à-dire, une forme compilée de la requête, qui est stockée par le fournisseur) lorsque vous appelez les méthodes [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) ou **Open**.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-112">If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) or **Open** methods.</span></span>

<span data-ttu-id="0b4cf-p103">En fonction du paramètre de la propriété [CommandType](commandtype-property-ado.md), ADO peut modifier la propriété **CommandText**. Vous pouvez lire la propriété **CommandText** à tout moment pour découvrir le texte réel de la commande utilisé par ADO au cours de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-p103">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property. You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="0b4cf-p104">Utilisez la propriété **CommandText** pour définir ou retourner une URL relative, spécifiant une ressource telle qu'un fichier ou un répertoire. La ressource est relative à un emplacement spécifié explicitement par une URL absolue ou spécifié implicitement par un objet [Connection](connection-object-ado.md) ouvert.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-p104">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory. The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0b4cf-p105">[!REMARQUE] Les URL utilisant le schéma HTTP appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, reportez-vous à la section <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</span><span class="sxs-lookup"><span data-stu-id="0b4cf-p105">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


