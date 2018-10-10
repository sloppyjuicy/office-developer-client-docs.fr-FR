---
title: Enregistrements et champs spécifiques au fournisseur
TOCTitle: Records and Provider-Supplied Fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6010c152691e80cad26c615851e4eef0193b4d0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469774"
---
# <a name="records-and-provider-supplied-fields"></a><span data-ttu-id="540c0-102">Enregistrements et champs spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="540c0-102">Records and Provider-Supplied Fields</span></span>


<span data-ttu-id="540c0-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="540c0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="540c0-104">Lorsqu'un objet [Record](record-object-ado.md) est ouvert, sa source peut être la ligne active d'un objet [Recordset](recordset-object-ado.md) ouvert, une URL absolue ou une URL relative à un objet [Connection](connection-object-ado.md) ouvert.</span><span class="sxs-lookup"><span data-stu-id="540c0-104">When a [Record](record-object-ado.md) object is opened, its source can be the current row of an open [Recordset](recordset-object-ado.md), an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="540c0-105">Si l'objet **Record** est ouvert depuis un objet **Recordset**, la collection **Fields** de l'objet [Record](fields-collection-ado.md) contiendra tous les champs provenant de l'objet **Recordset** ainsi que tous les champs ajoutés par le fournisseur sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="540c0-105">If the **Record** is opened from a **Recordset**, the **Record** object [Fields](fields-collection-ado.md) collection will contain all the fields from the **Recordset**, plus any fields added by the underlying provider.</span></span>

<span data-ttu-id="540c0-p101">Le fournisseur peut insérer d'autres champs utilisés comme caractéristiques supplémentaires de l'objet **Record**. Par conséquent, un objet **Record** peut comporter des champs uniques, non présents dans l'objet **Recordset** ou tout objet **Record** dérivé d'une autre ligne de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="540c0-p101">The provider may insert additional fields that serve as supplementary characteristics of the **Record**. As a result, a **Record** may have unique fields not in the **Recordset** as a whole or any **Record** derived from another row of the **Recordset**.</span></span>

<span data-ttu-id="540c0-p102">Par exemple, toutes les lignes d'un objet **Recordset** dérivé d'une source de données de messagerie électronique peuvent comporter des colonnes, telles que De, À et Objet. Un objet **Record** dérivé de cet objet **Recordset** comportera les mêmes champs. Cependant, l'objet **Record** peut également comporter d'autres champs uniques et spécifiques au message représenté par cet objet **Record**, Pièce jointe et CC, par exemple.</span><span class="sxs-lookup"><span data-stu-id="540c0-p102">For example, all rows of a **Recordset** derived from an e-mail data source might have columns such as From, To, and Subject. A **Record** derived from that **Recordset** will have the same fields. However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).</span></span>

<span data-ttu-id="540c0-111">Bien que l'objet **Record** et la ligne active de l'objet **Recordset** comportent les mêmes champs, ceux-ci diffèrent, car les objets **Record** et **Recordset** possèdent des méthodes et des propriétés différentes.</span><span class="sxs-lookup"><span data-stu-id="540c0-111">Although the **Record** object and current row of the **Recordset** have the same fields, they are different because **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="540c0-p103">Un champ commun aux objets **Record** et **Recordset** peut être modifié indifféremment dans l'un ou l'autre objet. Cependant, le champ ne peut pas être supprimé de l'objet **Record** même si le fournisseur sous-jacent accepte une valeur de champ null.</span><span class="sxs-lookup"><span data-stu-id="540c0-p103">A field held in common by the **Record** and **Recordset** can be modified on either object. However, the field cannot be deleted on the **Record** object, although the underlying provider may support setting the field to null.</span></span>

<span data-ttu-id="540c0-p104">Une fois que l'objet **Record** est ouvert, vous pouvez ajouter des champs par programme. Vous pouvez également supprimer ceux que vous avez ajoutés, mais vous ne pouvez pas supprimer les champs de l'objet **Recordset** initial.</span><span class="sxs-lookup"><span data-stu-id="540c0-p104">After the **Record** is opened, you can programmatically add fields. You can also delete fields you have added, but you cannot delete fields from the original **Recordset**.</span></span>

<span data-ttu-id="540c0-p105">Vous pouvez également ouvrir l'objet **Record** directement à partir d'une URL. Dans ce cas, les champs ajoutés à l'objet **Record** dépendent du fournisseur sous-jacent. Actuellement, la plupart des fournisseurs ajoutent un ensemble de champs qui décrivent l'entité représentée par l'objet **Record**. Si l'entité est constituée d'un flux d'octets, par exemple un fichier simple, un objet [Stream](stream-object-ado.md) peut généralement être ouvert depuis l'objet **Record**.</span><span class="sxs-lookup"><span data-stu-id="540c0-p105">You may also open the **Record** object directly from a URL. In this case, the fields added to the **Record** depend on the underlying provider. Currently, most providers add a set of fields that describe the entity represented by the **Record**. If the entity consists of a stream of bytes, such as a simple file, then a [Stream](stream-object-ado.md) object can usually be opened from the **Record**.</span></span>

## <a name="special-fields-for-document-source-providers"></a><span data-ttu-id="540c0-120">Champs spéciaux destinés aux fournisseurs de source de documents</span><span class="sxs-lookup"><span data-stu-id="540c0-120">Special Fields for Document Source Providers</span></span>

<span data-ttu-id="540c0-p106">Une classe spéciale de fournisseurs, appelée *fournisseurs de sources de documents*, gère les dossiers et les documents. Lorsqu'un objet **Record** représente un document ou qu'un objet **Recordset** représente un dossier de documents, le fournisseur de la source des documents remplit ces objets avec un jeu unique de champs qui décrivent les caractéristiques du document plutôt que le document en lui-même. En général, un champ contient une référence à l'objet **Stream** qui représente le document.</span><span class="sxs-lookup"><span data-stu-id="540c0-p106">A special class of providers, called *document source providers*, manages folders and documents. When a **Record** object represents a document or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself. Typically, one field contains a reference to the **Stream** that represents the document.</span></span>

<span data-ttu-id="540c0-124">Ces champs constituent un objet **Record** ou **Recordset** de ressources et sont répertoriés pour les fournisseurs spécifiques qui les prennent en charge à l' [Annexe A : Fournisseurs](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="540c0-124">These fields constitute a resource **record** or **recordset** and are listed for the specific providers that support them in [Appendix A: Providers](appendix-a-providers.md).</span></span>

<span data-ttu-id="540c0-p107">Deux constantes indexent la collection **Fields** d'un objet **Record** ou **Recordset** de ressources pour extraire une paire de champs fréquemment utilisés. La propriété **Value** de l'objet [Field](value-property-ado.md) retourne le contenu demandé.</span><span class="sxs-lookup"><span data-stu-id="540c0-p107">Two constants index the **Fields** collection of a resource **Record** or **Recordset** to retrieve a pair of commonly used fields. The **Field** object [Value](value-property-ado.md) property returns the desired content.</span></span>

  - <span data-ttu-id="540c0-p108">Le champ accédé avec la constante **adDefaultStream** contient un flux par défaut associé à l'objet **Record** ou **Recordset**. Le fournisseur affecte un flux par défaut à un objet.</span><span class="sxs-lookup"><span data-stu-id="540c0-p108">The field accessed with the **adDefaultStream** constant contains a default stream associated with the **Record** or **Recordset** object. The provider assigns a default stream to an object.</span></span>

  - <span data-ttu-id="540c0-129">Le champ accédé avec la constante **adRecordURL** contient l'URL absolue qui identifie le document.</span><span class="sxs-lookup"><span data-stu-id="540c0-129">The field accessed with the **adRecordURL** constant contains the absolute URL that identifies the document.</span></span>

<span data-ttu-id="540c0-p109">Un fournisseur de sources de documents ne prend pas en charge la collection [Properties](properties-collection-ado.md) des objets **Record** et **Field**. Le contenu de la collection **Properties** a une valeur null pour de tels objets.</span><span class="sxs-lookup"><span data-stu-id="540c0-p109">A document source provider does not support the [Properties](properties-collection-ado.md) collection of **Record** and **Field** objects. The content of the **Properties** collection is null for such objects.</span></span>

<span data-ttu-id="540c0-p110">Un fournisseur de sources de documents peut ajouter une propriété spécifique au fournisseur, comme la propriété **Datasource Type** qui permet de l'identifier. Pour plus d'informations sur la façon de déterminer le type de fournisseur, consultez la documentation de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="540c0-p110">A document source provider may add a provider-specific property such as **Datasource Type** to identify whether it is a document source provider. For more information about how to determine your type of provider, see your provider documentation.</span></span>

## <a name="resource-recordset-columns"></a><span data-ttu-id="540c0-134">Colonnes d'un objet Recordset de ressources</span><span class="sxs-lookup"><span data-stu-id="540c0-134">Resource Recordset Columns</span></span>

<span data-ttu-id="540c0-135">Un *objet Recordset de ressources* comporte les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="540c0-135">A *resource recordset* consists of the following columns.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="540c0-136">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="540c0-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="540c0-137">Type</span><span class="sxs-lookup"><span data-stu-id="540c0-137">Type</span></span></p></th>
<th><p><span data-ttu-id="540c0-138">Description</span><span class="sxs-lookup"><span data-stu-id="540c0-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="540c0-139">RESOURCE_PARSENAME</span><span class="sxs-lookup"><span data-stu-id="540c0-139">RESOURCE_PARSENAME</span></span></p></td>
<td><p><span data-ttu-id="540c0-140">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="540c0-140">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="540c0-p111">En lecture seule. Indique l'URL de la ressource.</span><span class="sxs-lookup"><span data-stu-id="540c0-p111">Read-only. Indicates the URL of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="540c0-143">RESOURCE_PARENTNAME</span><span class="sxs-lookup"><span data-stu-id="540c0-143">RESOURCE_PARENTNAME</span></span></p></td>
<td><p><span data-ttu-id="540c0-144">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="540c0-144">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="540c0-p112">En lecture seule. Indique l'URL absolue de l'enregistrement parent.</span><span class="sxs-lookup"><span data-stu-id="540c0-p112">Read-only. Indicates the absolute URL of the parent record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="540c0-147">RESOURCE_ABSOLUTEPARSENAME</span><span class="sxs-lookup"><span data-stu-id="540c0-147">RESOURCE_ABSOLUTEPARSENAME</span></span></p></td>
<td><p><span data-ttu-id="540c0-148">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="540c0-148">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="540c0-p113">En lecture seule. Indique l'URL absolue de la ressource, qui est la concaténation de PARENTNAME et PARSENAME.</span><span class="sxs-lookup"><span data-stu-id="540c0-p113">Read-only. Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="540c0-151">PROPRIÉTÉ RESOURCE_ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="540c0-151">RESOURCE_ISHIDDEN</span></span></p></td>
<td><p><span data-ttu-id="540c0-152">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="540c0-152">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="540c0-p114">True si la ressource est cachée. Aucune ligne n'est retournée sauf si la commande qui crée le jeu de lignes sélectionne de façon explicite les lignes dont la propriété RESOURCE_ISHIDDEN a la valeur True.</span><span class="sxs-lookup"><span data-stu-id="540c0-p114">True if the resource is hidden. No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="540c0-155">RESOURCE_ISREADONLY</span><span class="sxs-lookup"><span data-stu-id="540c0-155">RESOURCE_ISREADONLY</span></span></p></td>
<td><p><span data-ttu-id="540c0-156">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="540c0-156">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="540c0-p115">True si la ressource est en lecture seule. Tente d'ouvrir cette ressource avec DBBINDFLAG_WRITE et échoue avec DB_E_READONLY. Cette propriété peut être modifiée même si la ressource n'a été ouverte qu'en lecture.</span><span class="sxs-lookup"><span data-stu-id="540c0-p115">True if the resource is read-only. Attempts to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY. This property may be edited even when the resource has only been opened for reading.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="540c0-160">RESOURCE_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="540c0-160">RESOURCE_CONTENTTYPE</span></span></p></td>
<td><p><span data-ttu-id="540c0-161">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="540c0-161">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="540c0-162">Indique l’utilisation probable du document — par exemple, un dossier d’avocat.</span><span class="sxs-lookup"><span data-stu-id="540c0-162">Indicates the likely use of the document — for example, a lawyer's brief.</span></span> <span data-ttu-id="540c0-163">Cela peut correspondre au modèle Office utilisé pour créer le document.&quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="540c0-163">This may correspond to the Office template used to create the document.&quot;&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="540c0-164">RESOURCE_CONTENTCLASS</span><span class="sxs-lookup"><span data-stu-id="540c0-164">RESOURCE_CONTENTCLASS</span></span></p></td>
<td><p><span data-ttu-id="540c0-165">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="540c0-165">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="540c0-166">Indique le type MIME du document, spécifiant le format tel que &quot;texte/html&quot;. »</span><span class="sxs-lookup"><span data-stu-id="540c0-166">Indicates the MIME type of the document, indicating the format such as &quot;text/html&quot;.'</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="540c0-167">RESOURCE_CONTENTLANGUAGE</span><span class="sxs-lookup"><span data-stu-id="540c0-167">RESOURCE_CONTENTLANGUAGE</span></span></p></td>
<td><p><span data-ttu-id="540c0-168">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="540c0-168">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="540c0-169">Indique la langue dans laquelle le contenu est stocké.</span><span class="sxs-lookup"><span data-stu-id="540c0-169">Indicates the language in which the content is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="540c0-170">RESOURCE_CREATIONTIME</span><span class="sxs-lookup"><span data-stu-id="540c0-170">RESOURCE_CREATIONTIME</span></span></p></td>
<td><p><span data-ttu-id="540c0-171">adFileTime</span><span class="sxs-lookup"><span data-stu-id="540c0-171">adFileTime</span></span></p></td>
<td><p><span data-ttu-id="540c0-p117">En lecture seule. Indique une structure FILETIME contenant l'heure à laquelle la ressource a été créée. L'heure est au format de temps universel (UTC, Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="540c0-p117">Read-only. Indicates a FILETIME structure containing the time the resource was created. The time is reported in Coordinated Universal Time (UTC) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="540c0-175">RESOURCE_LASTACCESSTIME</span><span class="sxs-lookup"><span data-stu-id="540c0-175">RESOURCE_LASTACCESSTIME</span></span></p></td>
<td><p><span data-ttu-id="540c0-176">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="540c0-176">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="540c0-p118">En lecture seule. Indique une structure FILETIME contenant l'heure à laquelle la ressource a été créée. L'heure est au format UTC. Les membres FILETIME sont au nombre de zéro si le fournisseur ne prend pas en charge ce membre de temps.</span><span class="sxs-lookup"><span data-stu-id="540c0-p118">Read-only. Indicates a FILETIME structure containing the time that the resource was last accessed. The time is in UTC format. The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="540c0-181">RESOURCE_LASTWRITETIME</span><span class="sxs-lookup"><span data-stu-id="540c0-181">RESOURCE_LASTWRITETIME</span></span></p></td>
<td><p><span data-ttu-id="540c0-182">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="540c0-182">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="540c0-p119">En lecture seule. Indique une structure FILETIME contenant l'heure à laquelle la ressource a été créée. L'heure est au format UTC. Les membres FILETIME sont au nombre de zéro si le fournisseur ne prend pas en charge ce membre de temps.</span><span class="sxs-lookup"><span data-stu-id="540c0-p119">Read-only. Indicates a FILETIME structure containing the time that the resource was last written. The time is in UTC format. The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="540c0-187">RESOURCE_STREAMSIZE</span><span class="sxs-lookup"><span data-stu-id="540c0-187">RESOURCE_STREAMSIZE</span></span></p></td>
<td><p><span data-ttu-id="540c0-188">asUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="540c0-188">asUnsignedBigInt</span></span></p></td>
<td><p><span data-ttu-id="540c0-p120">En lecture seule. Indique la taille (en octets) du flux par défaut de la ressource.</span><span class="sxs-lookup"><span data-stu-id="540c0-p120">Read-only. Indicates the size of the resource's default stream, in bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="540c0-191">RESOURCE_ISCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="540c0-191">RESOURCE_ISCOLLECTION</span></span></p></td>
<td><p><span data-ttu-id="540c0-192">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="540c0-192">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="540c0-p121">En lecture seule. True si la ressource est une collection, telle qu'un répertoire. False si la ressource est un fichier simple.</span><span class="sxs-lookup"><span data-stu-id="540c0-p121">Read-only. True if the resource is a collection, such as a directory. False if the resource is a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="540c0-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span><span class="sxs-lookup"><span data-stu-id="540c0-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="540c0-197">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="540c0-197">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="540c0-p122">True si la ressource est un document structuré. False si la ressource n'est pas un document structuré. Il peut s'agir d'une collection ou d'un fichier simple.</span><span class="sxs-lookup"><span data-stu-id="540c0-p122">True if the resource is a structured document. False if the resource is not a structured document. It could be a collection or a simple file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="540c0-201">DEFAULT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="540c0-201">DEFAULT_DOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="540c0-202">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="540c0-202">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="540c0-p123">En lecture seule. Indique que cette ressource contient une URL pointant vers le document simple par défaut d'un dossier ou un document structuré. Utilisé si le flux par défaut est requis par une ressource. Pour les fichiers simples, cette propriété est vide.</span><span class="sxs-lookup"><span data-stu-id="540c0-p123">Read-only. Indicates that this resource contains a URL to the default simple document of a folder or a structured document. Used when the default stream is requested from a resource. This property is blank for a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="540c0-207">CHAPTERED_CHILDREN</span><span class="sxs-lookup"><span data-stu-id="540c0-207">CHAPTERED_CHILDREN</span></span></p></td>
<td><p><span data-ttu-id="540c0-208">AdChapter</span><span class="sxs-lookup"><span data-stu-id="540c0-208">AdChapter</span></span></p></td>
<td><p><span data-ttu-id="540c0-p124">En lecture seule. Facultative. Indique le chapitre du jeu de lignes contenant les enfants de la ressource. (Le <em>fournisseur Microsoft OLE DB pour la publication Internet</em> ne prend pas en charge cette colonne.)</span><span class="sxs-lookup"><span data-stu-id="540c0-p124">Read-only. Optional. Indicates the chapter of the rowset containing the children of the resource. (The <em>OLE DB Provider for Internet Publishing</em> does not use this column.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="540c0-213">RESOURCE_DISPLAYNAME</span><span class="sxs-lookup"><span data-stu-id="540c0-213">RESOURCE_DISPLAYNAME</span></span></p></td>
<td><p><span data-ttu-id="540c0-214">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="540c0-214">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="540c0-p125">En lecture seule. Indique le nom complet de la ressource.</span><span class="sxs-lookup"><span data-stu-id="540c0-p125">Read-only. Indicates the display name of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="540c0-217">RESOURCE_ISROOT</span><span class="sxs-lookup"><span data-stu-id="540c0-217">RESOURCE_ISROOT</span></span></p></td>
<td><p><span data-ttu-id="540c0-218">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="540c0-218">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="540c0-p126">En lecture seule. True si la ressource est la racine d'une collection ou d'un document structuré.</span><span class="sxs-lookup"><span data-stu-id="540c0-p126">Read-only. True if the resource is the root of a collection or structured document.</span></span></p></td>
</tr>
</tbody>
</table>

