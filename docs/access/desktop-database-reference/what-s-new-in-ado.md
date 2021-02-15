---
title: Nouveautés d’ActiveX Data Objects (ADO)
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 593daf08da1b4ce435d17f2a6deedfa3e89dbd32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302610"
---
# <a name="whats-new-in-ado"></a><span data-ttu-id="dbece-102">Nouveautés dans ADO</span><span class="sxs-lookup"><span data-stu-id="dbece-102">What's new in ADO</span></span>

<span data-ttu-id="dbece-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dbece-103">**Applies to**: Access 2013, Office 2013</span></span> 
 
<span data-ttu-id="dbece-104">La version ADO 2.5 propose les nouvelles fonctionnalités suivantes ainsi qu'une documentation enrichie.</span><span class="sxs-lookup"><span data-stu-id="dbece-104">The following new features and enhanced documentation are included in the ADO 2.5 release.</span></span> <span data-ttu-id="dbece-105">Cette liste englobe ADO, ADO MD et ADOX.</span><span class="sxs-lookup"><span data-stu-id="dbece-105">This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="dbece-106">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="dbece-106">New features</span></span>

- <span data-ttu-id="dbece-107">**[Enregistrements et flux](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="dbece-107">**[Records and streams](chapter-10-records-and-streams.md)**</span></span>

  <span data-ttu-id="dbece-108">Cette version d’ADO introduit l’objet [Record,](record-object-ado.md) qui peut représenter et gérer des éléments tels que des répertoires et des fichiers dans un système de fichiers, ainsi que des dossiers et des messages dans un système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="dbece-108">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an email system.</span></span> <span data-ttu-id="dbece-109">L'objet **Record** peut également représenter une ligne d'un [Recordset](recordset-object-ado.md), bien que les objets **Record** et **Recordset** aient des méthodes et des propriétés différentes.</span><span class="sxs-lookup"><span data-stu-id="dbece-109">A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

  <span data-ttu-id="dbece-110">Le nouvel objet [Stream](stream-object-ado.md) fournit les moyens de lire, d'écrire et de gérer le flux binaire d'octets ou de texte qui compose un flux de message ou de fichier.</span><span class="sxs-lookup"><span data-stu-id="dbece-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

- <span data-ttu-id="dbece-111">**[Utilisation des URL](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="dbece-111">**[URL usage](absolute-and-relative-urls.md)**</span></span>

  <span data-ttu-id="dbece-p103">Cette version introduit également l'utilisation d'URL (Uniform Resource Locators) à la place des chaînes de connexion et du texte de commande pour nommer des objets de magasin de données. Ces URL peuvent être employées avec les objets [Connection](connection-object-ado.md) et **Recordset** existants ainsi qu'avec les nouveaux objets **Record** et **Stream**.</span><span class="sxs-lookup"><span data-stu-id="dbece-p103">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects. URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

  <span data-ttu-id="dbece-p104">La nouvelle version d’ADO prend également en charge des fournisseurs OLE DB qui identifient leurs propres schémas d’URL. Par exemple, le [fournisseur OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md)*,* qui accède au système de fichiers Windows 2000, identifie le schéma HTTP existant.</span><span class="sxs-lookup"><span data-stu-id="dbece-p104">With this release, ADO supports OLE DB providers that recognize their own URL schemes. For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

- <span data-ttu-id="dbece-116">**[Champs spéciaux pour les fournisseurs de sources de documents](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="dbece-116">**[Special fields for document source providers](records-and-provider-supplied-fields.md)**</span></span>

  <span data-ttu-id="dbece-117">Une classe spéciale de fournisseurs, appelée fournisseurs de *source de documents*, gère des dossiers et des documents.</span><span class="sxs-lookup"><span data-stu-id="dbece-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="dbece-118">Lorsqu'un objet **Record** représente un document ou lorsqu'un objet **Recordset** représente un dossier de documents, le fournisseur de source de documents remplit ces objets d'un ensemble de champs unique qui décrit les caractéristiques du document.</span><span class="sxs-lookup"><span data-stu-id="dbece-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="dbece-119">Ces champs constituent un *enregistrement de ressource*  ou **un recordset**.</span><span class="sxs-lookup"><span data-stu-id="dbece-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="dbece-120">Nouvelles rubriques de référence</span><span class="sxs-lookup"><span data-stu-id="dbece-120">New reference topics</span></span>

### <a name="properties"></a><span data-ttu-id="dbece-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dbece-121">Properties</span></span>

<span data-ttu-id="dbece-122">Les nouvelles propriétés suivantes sont fournies dans cette version.</span><span class="sxs-lookup"><span data-stu-id="dbece-122">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dbece-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="dbece-123">Property</span></span></p></th>
<th><p><span data-ttu-id="dbece-124">Description</span><span class="sxs-lookup"><span data-stu-id="dbece-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbece-125"><a href="charset-property-ado.md">Charset</a></span><span class="sxs-lookup"><span data-stu-id="dbece-125"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-126">Indique dans quel jeu de caractères le contenu d'un objet <strong>Stream</strong> de texte doit être traduit.</span><span class="sxs-lookup"><span data-stu-id="dbece-126">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-127"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="dbece-127"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-128">Indique si la position actuelle correspond à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="dbece-128">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="dbece-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-130">Indique quel caractère binaire utiliser comme séparateur de ligne dans des objets <strong>Stream</strong> de texte.</span><span class="sxs-lookup"><span data-stu-id="dbece-130">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-131"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="dbece-131"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-132">Indique les autorisations disponibles pour modifier les données d'un objet <strong>Connection</strong>, <strong>Record</strong> ou <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="dbece-132">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-133"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="dbece-133"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-134">Indique la chaîne d'URL absolue qui pointe vers l'objet <strong>Record</strong> parent de l'objet <strong>Record</strong> actif.</span><span class="sxs-lookup"><span data-stu-id="dbece-134">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-135"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="dbece-135"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-136">Indique la position actuelle dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="dbece-136">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-137"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="dbece-137"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-138">Indique le type de l'objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="dbece-138">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Taille</a></span><span class="sxs-lookup"><span data-stu-id="dbece-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-140">Indique la taille du flux en nombre d'octets.</span><span class="sxs-lookup"><span data-stu-id="dbece-140">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-141"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="dbece-141"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-142">Indique l'entité représentée par l'objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="dbece-142">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-143"><a href="state-property-ado.md">État</a></span><span class="sxs-lookup"><span data-stu-id="dbece-143"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-144">Indique, pour tous les objets applicables, si l'état de l'objet est ouvert ou fermé.</span><span class="sxs-lookup"><span data-stu-id="dbece-144">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="dbece-145">Indique, pour tous les objets applicables exécutant une méthode asynchrone, si l'état actuel de l'objet est « en cours de connexion », « en cours d'exécution » ou « en cours d'extraction ».</span><span class="sxs-lookup"><span data-stu-id="dbece-145">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-146"><a href="type-property-ado-stream.md">Type (Type)</a></span><span class="sxs-lookup"><span data-stu-id="dbece-146"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-147">Indique le type des données contenues dans l'objet <strong>Stream</strong> (binaire ou texte).</span><span class="sxs-lookup"><span data-stu-id="dbece-147">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a><span data-ttu-id="dbece-148">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dbece-148">Methods</span></span>

<span data-ttu-id="dbece-149">Les nouvelles méthodes suivantes sont fournies dans cette version.</span><span class="sxs-lookup"><span data-stu-id="dbece-149">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dbece-150">Méthode</span><span class="sxs-lookup"><span data-stu-id="dbece-150">Method</span></span></p></th>
<th><p><span data-ttu-id="dbece-151">Description</span><span class="sxs-lookup"><span data-stu-id="dbece-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbece-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="dbece-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-153">Copie un fichier ou un répertoire, ainsi que son contenu à un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="dbece-153">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-154"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="dbece-154"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-155">Copie le nombre spécifié de caractères ou d’octets (selon <strong>le type)</strong>de l’objet <strong>Stream</strong> <strong>dans</strong> un <strong>autre objet Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="dbece-155">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="dbece-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-157">Supprime un fichier ou un répertoire avec tous ses sous-répertoires.</span><span class="sxs-lookup"><span data-stu-id="dbece-157">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-158"><a href="flush-method-ado.md">Flush</a></span><span class="sxs-lookup"><span data-stu-id="dbece-158"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-159">Force le contenu de l'objet <strong>Stream</strong> encore présent dans la mémoire tampon ADO dans l'objet sous-jacent auquel cet objet <strong>Stream</strong> est associé.</span><span class="sxs-lookup"><span data-stu-id="dbece-159">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-160"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="dbece-160"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-161">Retourne un objet <strong>Recordset</strong> dont les lignes représentent les fichiers et sous-répertoires du répertoire représenté par cet objet <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="dbece-161">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="dbece-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-163">Charge le contenu d'un fichier existant dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="dbece-163">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-164"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="dbece-164"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-165">Déplace un fichier ou un répertoire, avec tout son contenu, vers un autre emplacement.</span><span class="sxs-lookup"><span data-stu-id="dbece-165">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-166"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="dbece-166"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-167">Ouvre un objet <strong>Record</strong> existant ou crée un fichier ou un répertoire.</span><span class="sxs-lookup"><span data-stu-id="dbece-167">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-168"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="dbece-168"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-169">Ouvre un objet <strong>Stream</strong> afin de manipuler des flux de données binaires ou de texte.</span><span class="sxs-lookup"><span data-stu-id="dbece-169">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-170"><a href="read-method-ado.md">Lire</a></span><span class="sxs-lookup"><span data-stu-id="dbece-170"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-171">Lit le nombre spécifié d'octets d'un objet <strong>Stream</strong> binaire.</span><span class="sxs-lookup"><span data-stu-id="dbece-171">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-172"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="dbece-172"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-173">Lit le nombre spécifié de caractères d'un objet <strong>Stream</strong> de texte.</span><span class="sxs-lookup"><span data-stu-id="dbece-173">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-174"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="dbece-174"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-175">Enregistre le contenu binaire d'un objet <strong>Stream</strong> dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="dbece-175">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-176"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="dbece-176"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-177">Définit la position qui correspond à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="dbece-177">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-178"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="dbece-178"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-179">Saute une ligne complète lors de la lecture d'un objet <strong>Stream</strong> de texte.</span><span class="sxs-lookup"><span data-stu-id="dbece-179">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dbece-180"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="dbece-180"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-181">Écrit des données binaires dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="dbece-181">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbece-182"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="dbece-182"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="dbece-183">Écrit une chaîne de texte spécifiée dans un objet <strong>Stream</strong>.</span><span class="sxs-lookup"><span data-stu-id="dbece-183">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="dbece-184">Documentation nouvelle et améliorée</span><span class="sxs-lookup"><span data-stu-id="dbece-184">New and enhanced documentation</span></span>

- <span data-ttu-id="dbece-185">**[Rubriques d’exemples de code](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="dbece-185">**[Code example topics](ado-code-examples.md)**</span></span>

  <span data-ttu-id="dbece-186">Les exemples ont été développés pour contenir des exemples de code écrits en Microsoft Visual C++ et Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="dbece-186">The examples have been expanded to contain code examples written in Microsoft Visual C++ and Microsoft Visual J++.</span></span> <span data-ttu-id="dbece-187">Vous pouvez copier et coller ces exemples dans votre éditeur.</span><span class="sxs-lookup"><span data-stu-id="dbece-187">You can copy and paste these code examples into your editor.</span></span>

- <span data-ttu-id="dbece-188">**[Rubriques sur le fournisseur](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="dbece-188">**[Provider topics](appendix-a-providers.md)**</span></span>

  <span data-ttu-id="dbece-189">Une nouvelle rubrique, qui explique comment utiliser ADO avec le [fournisseur OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md), a été ajoutée.</span><span class="sxs-lookup"><span data-stu-id="dbece-189">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

- <span data-ttu-id="dbece-190">**[Programmation avec ADO](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="dbece-190">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

  <span data-ttu-id="dbece-191">Cette nouvelle section contient des conseils et des astuces pour l'utilisation d'ADO avec différents langages de programmation.</span><span class="sxs-lookup"><span data-stu-id="dbece-191">This new section contains tips and tricks for using ADO with various programming languages.</span></span> <span data-ttu-id="dbece-192">Il contient les index de syntaxe existants pour les extensions Visual C++ pour ADO et ADO/WFC, ainsi que de nouvelles informations spécifiques aux développeurs qui utilisent Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++ ou Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="dbece-192">It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, or Microsoft Visual J++.</span></span>

