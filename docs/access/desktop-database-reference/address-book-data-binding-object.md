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
# <a name="address-book-data-binding-object"></a>Objet de liaison de données du carnet d'adresses


**S’applique à**: Access 2013, Office 2013

L'application Carnet d'adresses utilise l'objet [RDS.DataControl](datacontrol-object-rds.md) pour lier les données de la base de données SQL Server à un objet visuel (dans le cas présent, un tableau DHTML) dans la page HTML cliente de l'application. La logique de programmation événementielle de VBScript utilise l'objet [RDS.DataControl](datacontrol-object-rds.md) pour :

  - interroger la base de données, lui envoyer des mises à jour et actualiser la grille de données ;

  - autoriser des utilisateurs à accéder au premier ou dernier enregistrement ainsi qu'à l'enregistrement suivant ou précédent de la grille de données.

L'exemple de code suivant définit le composant **RDS.DataControl**:

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

La balise OBJECT définit le composant **RDS.DataControl** dans le programme. Elle inclut deux types de paramètres :

  - ceux associés à la balise OBJECT générique ;

  - ceux propres à l'objet **RDS.DataControl**.

## <a name="generic-object-tag-parameters"></a>Paramètres de la balise OBJECT générique

Le tableau suivant décrit les paramètres associés à la balise OBJECT.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Paramètre</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><em>CLASSID</em></strong></p></td>
<td><p>Nombre 128 bits unique qui permet au système d’identifier le type d’objet incorporé. Cet identificateur est conservé dans le Registre système de l’ordinateur local. (Pour en savoir plus sur les ID de classe de l’objet <strong>RDS.DataControl</strong>, consultez <a href="datacontrol-object-rds.md">RDS.DataControl, objet</a>).</p></td>
</tr>
<tr class="even">
<td><p><strong><em>ID</em></strong></p></td>
<td><p>Définit un identificateur de niveau document permettant d'identifier l'objet incorporé dans le code.</p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a>Paramètres de la balise RDS.DataControl

Le tableau suivant décrit les paramètres spécifiques à l'objet **RDS.DataControl**. (Pour obtenir une liste complète des paramètres de l'objet **RDS.DataControl** et savoir quand les implémenter, consultez [RDS.DataControl, objet](datacontrol-object-rds.md)).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Paramètre</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="server-property-rds.md">SERVEUR</a></p></td>
<td><p>Si vous utilisez HTTP, la valeur est le nom de l’ordinateur serveur précédé par https://.</p></td>
</tr>
<tr class="even">
<td><p><a href="connect-property-rds.md">SE CONNECTER</a></p></td>
<td><p>Fournit les informations de connexion nécessaires pour la connexion de l'objet <strong>RDS.DataControl</strong> à SQL Server.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/jj248989(v=office.15)">SQL</a></p></td>
<td><p>Définit ou retourne la chaîne de requête utilisée pour récupérer l’objet <a href="recordset-object-ado.md">Recordset</a>.</p></td>
</tr>
</tbody>
</table>

