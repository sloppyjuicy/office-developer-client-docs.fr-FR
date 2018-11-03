---
title: Objet de liaison de données du carnet d'adresses
TOCTitle: Address Book Data-Binding object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f90a0e4ff4accfd4496df46fb48faaf6f589f37c
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945180"
---
# <a name="address-book-data-binding-object"></a><span data-ttu-id="1d262-102">Objet de liaison de données du carnet d'adresses</span><span class="sxs-lookup"><span data-stu-id="1d262-102">Address Book Data-Binding object</span></span>


<span data-ttu-id="1d262-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d262-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d262-p101">L'application Carnet d'adresses utilise l'objet [RDS.DataControl](datacontrol-object-rds.md) pour lier les données de la base de données SQL Server à un objet visuel (dans le cas présent, un tableau DHTML) dans la page HTML cliente de l'application. La logique de programmation événementielle de VBScript utilise l'objet [RDS.DataControl](datacontrol-object-rds.md) pour :</span><span class="sxs-lookup"><span data-stu-id="1d262-p101">The Address Book application uses the [RDS.DataControl](datacontrol-object-rds.md) object to bind data from the SQL Server database to a visual object (in this case, a DHTML table) in the application's client HTML page. The event-driven VBScript program logic uses the [RDS.DataControl](datacontrol-object-rds.md) to:</span></span>

  - <span data-ttu-id="1d262-106">interroger la base de données, lui envoyer des mises à jour et actualiser la grille de données ;</span><span class="sxs-lookup"><span data-stu-id="1d262-106">Query the database, send updates to the database, and refresh the data grid.</span></span>

  - <span data-ttu-id="1d262-107">autoriser des utilisateurs à accéder au premier ou dernier enregistrement ainsi qu'à l'enregistrement suivant ou précédent de la grille de données.</span><span class="sxs-lookup"><span data-stu-id="1d262-107">Allow users to move to the first, next, previous, or last record in the data grid.</span></span>

<span data-ttu-id="1d262-108">L'exemple de code suivant définit le composant **RDS.DataControl**:</span><span class="sxs-lookup"><span data-stu-id="1d262-108">The following code defines the **RDS.DataControl** component:</span></span>

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

<span data-ttu-id="1d262-p102">La balise OBJECT définit le composant **RDS.DataControl** dans le programme. Elle inclut deux types de paramètres :</span><span class="sxs-lookup"><span data-stu-id="1d262-p102">The OBJECT tag defines the **RDS.DataControl** component in the program. The tag includes two types of parameters:</span></span>

  - <span data-ttu-id="1d262-111">ceux associés à la balise OBJECT générique ;</span><span class="sxs-lookup"><span data-stu-id="1d262-111">Those associated with the generic OBJECT tag.</span></span>

  - <span data-ttu-id="1d262-112">ceux propres à l'objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="1d262-112">Those specific to the **RDS.DataControl** object.</span></span>

## <a name="generic-object-tag-parameters"></a><span data-ttu-id="1d262-113">Paramètres de la balise OBJECT générique</span><span class="sxs-lookup"><span data-stu-id="1d262-113">Generic OBJECT Tag Parameters</span></span>

<span data-ttu-id="1d262-114">Le tableau suivant décrit les paramètres associés à la balise OBJECT.</span><span class="sxs-lookup"><span data-stu-id="1d262-114">The following table describes the parameters associated with the OBJECT tag.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d262-115">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1d262-115">Parameter</span></span></p></th>
<th><p><span data-ttu-id="1d262-116">Description</span><span class="sxs-lookup"><span data-stu-id="1d262-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d262-117"><strong><em>CLASSID</em></strong></span><span class="sxs-lookup"><span data-stu-id="1d262-117"><strong><em>CLASSID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="1d262-p103">Nombre 128 bits unique qui permet au système d’identifier le type d’objet incorporé. Cet identificateur est conservé dans le Registre système de l’ordinateur local. (Pour en savoir plus sur les ID de classe de l’objet <strong>RDS.DataControl</strong>, consultez <a href="datacontrol-object-rds.md">RDS.DataControl, objet</a>).</span><span class="sxs-lookup"><span data-stu-id="1d262-p103">A unique, 128-bit number that identifies the type of embedded object to the system. This identifier is maintained in the local computer's system registry. (For the class IDs of the <strong>RDS.DataControl</strong> object, see <a href="datacontrol-object-rds.md">RDS.DataControl Object</a>.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d262-121"><strong><em>ID</em></strong></span><span class="sxs-lookup"><span data-stu-id="1d262-121"><strong><em>ID</em></strong></span></span></p></td>
<td><p><span data-ttu-id="1d262-122">Définit un identificateur de niveau document permettant d'identifier l'objet incorporé dans le code.</span><span class="sxs-lookup"><span data-stu-id="1d262-122">Defines a document-wide identifier for the embedded object that is used to identify it in code.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a><span data-ttu-id="1d262-123">Paramètres de la balise RDS.DataControl</span><span class="sxs-lookup"><span data-stu-id="1d262-123">RDS.DataControl Tag Parameters</span></span>

<span data-ttu-id="1d262-p104">Le tableau suivant décrit les paramètres spécifiques à l'objet **RDS.DataControl**. (Pour obtenir une liste complète des paramètres de l'objet **RDS.DataControl** et savoir quand les implémenter, consultez [RDS.DataControl, objet](datacontrol-object-rds.md)).</span><span class="sxs-lookup"><span data-stu-id="1d262-p104">The following table describes the parameters specific to the **RDS.DataControl** object. (For a complete list of the **RDS.DataControl** object parameters, and when to implement them, see [RDS.DataControl object](datacontrol-object-rds.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1d262-126">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1d262-126">Parameter</span></span></p></th>
<th><p><span data-ttu-id="1d262-127">Description</span><span class="sxs-lookup"><span data-stu-id="1d262-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d262-128"><a href="server-property-rds.md">SERVEUR</a></span><span class="sxs-lookup"><span data-stu-id="1d262-128"><a href="server-property-rds.md">SERVER</a></span></span></p></td>
<td><p><span data-ttu-id="1d262-129">Si vous utilisez HTTP, la valeur est le nom de l’ordinateur serveur précédé par https://.</span><span class="sxs-lookup"><span data-stu-id="1d262-129">If you are using HTTP, the value is the name of the server computer preceded by https:// .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d262-130"><a href="connect-property-rds.md">SE CONNECTER</a></span><span class="sxs-lookup"><span data-stu-id="1d262-130"><a href="connect-property-rds.md">CONNECT</a></span></span></p></td>
<td><p><span data-ttu-id="1d262-131">Fournit les informations de connexion nécessaires pour la connexion de l'objet <strong>RDS.DataControl</strong> à SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1d262-131">Provides the necessary connection information for the <strong>RDS.DataControl</strong> to connect to SQL Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1d262-132"><a href="https://msdn.microsoft.com/library/jj248989(v=office.15)">SQL</a></span><span class="sxs-lookup"><span data-stu-id="1d262-132"><a href="https://msdn.microsoft.com/library/jj248989(v=office.15)">SQL</a></span></span></p></td>
<td><p><span data-ttu-id="1d262-133">Définit ou retourne la chaîne de requête utilisée pour récupérer l’objet <a href="recordset-object-ado.md">Recordset</a>.</span><span class="sxs-lookup"><span data-stu-id="1d262-133">Sets or returns the query string used to retrieve the <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
</tbody>
</table>

