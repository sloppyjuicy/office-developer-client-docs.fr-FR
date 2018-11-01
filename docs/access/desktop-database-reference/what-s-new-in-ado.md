---
title: Nouveautés dans les objets de données ActiveX (ADO)
TOCTitle: What's New in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5f374abd42659708ddb1e9fcd131faaac94f05cf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891113"
---
# <a name="whats-new-in-ado"></a><span data-ttu-id="41eea-102">Nouveautés dans ADO</span><span class="sxs-lookup"><span data-stu-id="41eea-102">What's New in ADO</span></span>


<span data-ttu-id="41eea-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="41eea-103">**Applies to**: Access 2013, Office 2013</span></span> 
 

<span data-ttu-id="41eea-p101">La version ADO 2.5 propose les nouvelles fonctionnalités suivantes ainsi qu'une documentation enrichie. Cette liste englobe ADO, ADO MD et ADOX.</span><span class="sxs-lookup"><span data-stu-id="41eea-p101">The following new features and enhanced documentation are included in the ADO 2.5 release. This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="41eea-106">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="41eea-106">New Features</span></span>

<span data-ttu-id="41eea-107">**[Enregistrements et flux](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="41eea-107">**[Records and Streams](chapter-10-records-and-streams.md)**</span></span>

<span data-ttu-id="41eea-p102">Cette nouvelle version d'ADO introduit l'objet [Record](record-object-ado.md), qui peut représenter et gérer des éléments comme les répertoires et fichiers d'un système de fichiers et les dossiers et messages d'un système de messagerie. L'objet **Record** peut également représenter une ligne d'un [Recordset](recordset-object-ado.md), bien que les objets **Record** et **Recordset** aient des méthodes et des propriétés différentes.</span><span class="sxs-lookup"><span data-stu-id="41eea-p102">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an e-mail system. A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="41eea-110">Le nouvel objet [Stream](stream-object-ado.md) fournit les moyens de lire, d'écrire et de gérer le flux binaire d'octets ou de texte qui compose un flux de message ou de fichier.</span><span class="sxs-lookup"><span data-stu-id="41eea-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

<span data-ttu-id="41eea-111">**[Utilisation d'URL](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="41eea-111">**[URL Usage](absolute-and-relative-urls.md)**</span></span>

<span data-ttu-id="41eea-p103">Cette version introduit également l'utilisation d'URL (Uniform Resource Locators) à la place des chaînes de connexion et du texte de commande pour nommer des objets de magasin de données. Ces URL peuvent être employées avec les objets [Connection](connection-object-ado.md) et **Recordset** existants ainsi qu'avec les nouveaux objets **Record** et **Stream**.</span><span class="sxs-lookup"><span data-stu-id="41eea-p103">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects. URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

<span data-ttu-id="41eea-p104">La nouvelle version d’ADO prend également en charge des fournisseurs OLE DB qui identifient leurs propres schémas d’URL. Par exemple, le [fournisseur OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md)*,* qui accède au système de fichiers Windows 2000, identifie le schéma HTTP existant.</span><span class="sxs-lookup"><span data-stu-id="41eea-p104">With this release, ADO supports OLE DB providers that recognize their own URL schemes. For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

<span data-ttu-id="41eea-116">**[Champs spéciaux pour les fournisseurs de source de documents](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="41eea-116">**[Special Fields for Document Source Providers](records-and-provider-supplied-fields.md)**</span></span>

<span data-ttu-id="41eea-117">Une classe spéciale de fournisseurs, appelée fournisseurs de *sources de documents* , gérer les documents et dossiers.</span><span class="sxs-lookup"><span data-stu-id="41eea-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="41eea-118">Lorsqu'un objet **Record** représente un document ou lorsqu'un objet **Recordset** représente un dossier de documents, le fournisseur de source de documents remplit ces objets d'un ensemble de champs unique qui décrit les caractéristiques du document.</span><span class="sxs-lookup"><span data-stu-id="41eea-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="41eea-119">Ces champs constituent une *ressource* **Record** ou **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="41eea-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="41eea-120">Nouvelles rubriques de référence</span><span class="sxs-lookup"><span data-stu-id="41eea-120">New Reference Topics</span></span>

<span data-ttu-id="41eea-121">Les nouvelles propriétés suivantes sont fournies dans cette version.</span><span class="sxs-lookup"><span data-stu-id="41eea-121">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41eea-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="41eea-122">Property</span></span></p></th>
<th><p><span data-ttu-id="41eea-123">Description</span><span class="sxs-lookup"><span data-stu-id="41eea-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41eea-124"><a href="charset-property-ado.md">Jeu de caractères</a></span><span class="sxs-lookup"><span data-stu-id="41eea-124"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-125">Indique dans quel jeu de caractères le contenu d'un objet <strong>Stream</strong> de texte doit être traduit.</span><span class="sxs-lookup"><span data-stu-id="41eea-125">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-126"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="41eea-126"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-127">Indique si la position actuelle est à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="41eea-127">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-128"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="41eea-128"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-129">Indique le caractère binaire à utiliser comme le séparateur de ligne dans des objets <strong>Stream</strong> textuels.</span><span class="sxs-lookup"><span data-stu-id="41eea-129">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-130"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="41eea-130"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-131">Indique les autorisations disponibles pour la modification des données d'un objet <strong>Connection</strong>, <strong>Enregistrement</strong> ou <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="41eea-131">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-132"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="41eea-132"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-133">Indique la chaîne d'URL absolue qui pointe vers l'objet <strong>Record</strong> parent de l'objet <strong>Record</strong> actif.</span><span class="sxs-lookup"><span data-stu-id="41eea-133">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-134"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="41eea-134"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-135">Indique la position actuelle dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="41eea-135">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-136"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="41eea-136"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-137">Indique le type de l'objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="41eea-137">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-138"><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Taille</a></span><span class="sxs-lookup"><span data-stu-id="41eea-138"><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Size</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-139">Indique la taille du flux en nombre d'octets.</span><span class="sxs-lookup"><span data-stu-id="41eea-139">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-140"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="41eea-140"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-141">Indique l'entité représentée par l'objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="41eea-141">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-142"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="41eea-142"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-143">Indique, pour tous les objets applicables, si l'état de l'objet est ouvert ou fermé.</span><span class="sxs-lookup"><span data-stu-id="41eea-143">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="41eea-144">Indique, pour tous les objets applicables exécutant une méthode asynchrone, si l'état actuel de l'objet est « en cours de connexion », « en cours d'exécution » ou « en cours d'extraction ».</span><span class="sxs-lookup"><span data-stu-id="41eea-144">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-145"><a href="type-property-ado-stream.md">Type</a></span><span class="sxs-lookup"><span data-stu-id="41eea-145"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-146">Indique le type des données contenues dans l'objet <strong>Stream</strong> (binaire ou texte).</span><span class="sxs-lookup"><span data-stu-id="41eea-146">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="41eea-147">Les nouvelles méthodes suivantes sont fournies dans cette version.</span><span class="sxs-lookup"><span data-stu-id="41eea-147">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41eea-148">Méthode</span><span class="sxs-lookup"><span data-stu-id="41eea-148">Method</span></span></p></th>
<th><p><span data-ttu-id="41eea-149">Description</span><span class="sxs-lookup"><span data-stu-id="41eea-149">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41eea-150"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="41eea-150"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-151">Copie un fichier ou un répertoire, avec tout son contenu, dans un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="41eea-151">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-152"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="41eea-152"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-153">Copie le nombre spécifié de caractères ou d’octets (selon le <strong>Type</strong>) dans <strong>l’objet</strong> <strong>flux de données</strong> à un autre objet <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="41eea-153">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-154"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="41eea-154"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-155">Supprime un fichier ou un répertoire avec tous ses sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="41eea-155">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-156"><a href="flush-method-ado.md">Vider</a></span><span class="sxs-lookup"><span data-stu-id="41eea-156"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-157">Force le contenu de l'objet <strong>Stream</strong> encore présent dans la mémoire tampon ADO dans l'objet sous-jacent auquel cet objet <strong>Stream</strong> est associé.</span><span class="sxs-lookup"><span data-stu-id="41eea-157">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-158"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="41eea-158"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-159">Retourne un objet <strong>Recordset</strong> dont les lignes représentent les fichiers et sous-répertoires du répertoire représenté par cet objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="41eea-159">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-160"><a href="loadfromfile-method-ado.md">La méthode LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="41eea-160"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-161">Charge le contenu d'un fichier existant dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="41eea-161">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-162"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="41eea-162"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-163">Déplace un fichier ou un répertoire, avec tout son contenu, vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="41eea-163">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-164"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="41eea-164"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-165">Ouvre un objet <strong>Record</strong> existant ou crée un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="41eea-165">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-166"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="41eea-166"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-167">Ouvre un objet <strong>Stream</strong> pour manipuler des flux de données binaires ou de texte.</span><span class="sxs-lookup"><span data-stu-id="41eea-167">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-168"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="41eea-168"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-169">Lit un nombre spécifié d'octets dans un objet <strong>Stream</strong> binaire.</span><span class="sxs-lookup"><span data-stu-id="41eea-169">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-170"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="41eea-170"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-171">Lit un nombre spécifié de caractères dans un objet <strong>Stream</strong> de texte.</span><span class="sxs-lookup"><span data-stu-id="41eea-171">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-172"><a href="savetofile-method-ado.md">Méthode SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="41eea-172"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-173">Enregistre le contenu binaire d'un objet <strong>Stream</strong> dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="41eea-173">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-174"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="41eea-174"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-175">Définit la position qui représente la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="41eea-175">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-176"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="41eea-176"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-177">Saute une ligne complète lors de la lecture d'un objet <strong>Stream</strong> de texte.</span><span class="sxs-lookup"><span data-stu-id="41eea-177">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41eea-178"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="41eea-178"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-179">Écrit des données binaires dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="41eea-179">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41eea-180"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="41eea-180"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="41eea-181">Écrit une chaîne de texte spécifiée dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="41eea-181">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="41eea-182">Nouvelle documentation et documentation enrichie</span><span class="sxs-lookup"><span data-stu-id="41eea-182">New and Enhanced Documentation</span></span>

<span data-ttu-id="41eea-183">**[Rubriques d'exemples de codes](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="41eea-183">**[Code Example Topics](ado-code-examples.md)**</span></span>

<span data-ttu-id="41eea-p107">La documentation contient maintenant des exemples de codes écrits en Microsoft Visual C++® et en Microsoft Visual J++®. Vous pouvez copier et coller ces exemples dans votre éditeur.</span><span class="sxs-lookup"><span data-stu-id="41eea-p107">The examples have been expanded to contain code examples written in Microsoft Visual C++® and Microsoft Visual J++®. You can copy and paste these code examples into your editor.</span></span>

<span data-ttu-id="41eea-186">**[Rubriques relatives aux fournisseurs](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="41eea-186">**[Provider Topics](appendix-a-providers.md)**</span></span>

<span data-ttu-id="41eea-187">Une nouvelle rubrique, qui explique comment utiliser ADO avec le [fournisseur OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md), a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="41eea-187">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

<span data-ttu-id="41eea-188">**[Programmation avec ADO](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="41eea-188">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

<span data-ttu-id="41eea-p108">Cette nouvelle section contient des conseils et des astuces pour l'utilisation d'ADO avec différents langages de programmation. Elle comporte les index de syntaxes existants pour les extensions Visual C++ pour ADO et ADO/WFC et propose des informations destinées aux développeurs qui utilisent Microsoft Visual Basic®, Microsoft Visual Basic® Scripting Edition, Microsoft JScript®, Microsoft Visual C++ ou Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="41eea-p108">This new section contains tips and tricks for using ADO with various programming languages. It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic®, Microsoft Visual Basic® Scripting Edition, Microsoft JScript®, Microsoft Visual C++, or Microsoft Visual J++.</span></span>

