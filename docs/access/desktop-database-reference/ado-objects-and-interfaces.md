---
title: Objets et interfaces ADO
TOCTitle: ADO objects and interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 92599e81fcaf1303bd1c77c1d6f09acfe5dd63a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553234"
---
# <a name="ado-objects-and-interfaces"></a>Objets et interfaces ADO

**S’applique à** : Access 2013, Office 2013

Les relations entre ces objets sont représentées dans le ActiveX objet Data Objects (ADO).

Chaque objet peut être contenu dans sa collection correspondante. Un objet [Error](error-object-ado.md) peut, par exemple, être contenu dans une collection [Errors](errors-collection-ado.md). Pour plus d’informations, voir [les collections ADO](ado-collections.md) ou une rubrique de collection spécifique.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Objet</th>
<th>Description</th>
</tr>
<tr class="odd">
<td><p><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></p></td>
<td><p>Crée un objet <strong>Record</strong> ADO à partir d'un objet <strong>Row</strong> OLE DB dans une application C/C++.</p></td>
</tr>
<tr class="even">
<td><p><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></p></td>
<td><p>Crée un objet <strong>Recordset</strong> ADO à partir d'un objet <strong>Rowset</strong> OLE DB dans une application C/C++.</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Command</a></p></td>
<td><p>Définit une commande spécifique que vous avez l'intention d'exécuter sur une source de données.</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Connection</a></p></td>
<td><p>Représente une connexion ouverte à une source de données.</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Erreur</a></p></td>
<td><p>Contient le détail des erreurs d'accès aux données concernant une même opération liée au fournisseur.</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Field</a></p></td>
<td><p>Représente une colonne de données avec un type de données commun.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameter-object-ado.md">Paramètre</a></p></td>
<td><p>Représente un paramètre ou un argument associé à un objet <strong>Command </strong> basé sur une requête paramétrée ou une procédure stockée.</p></td>
</tr>
<tr class="even">
<td><p><a href="property-object-ado.md">Propriété</a></p></td>
<td><p>Représente une caractéristique dynamique d'un objet ADO qui est définie par le fournisseur.</p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Record</a></p></td>
<td><p>Représente une ligne d'un objet <strong>Recordset</strong> ou un répertoire ou un fichier dans un système de fichiers.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Recordset</a></p></td>
<td><p>Représente le jeu entier d'enregistrements d'une table de base ou les résultats d'une commande exécutée. L'objet <strong>Recordset</strong> ne peut faire référence qu'à un seul enregistrement à l'intérieur du jeu en tant qu'enregistrement actif.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p>Représente un flux binaire de données.</p></td>
</tr>
</tbody>
</table>

<br/>

