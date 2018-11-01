---
title: Objets et interfaces ADO
TOCTitle: ADO Objects and Interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efab7ce2980393282ee1f96295206e712fcbd15f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882181"
---
# <a name="ado-objects-and-interfaces"></a>Objets et interfaces ADO


**S’applique à**: Access 2013, Office 2013

Les relations entre ces objets sont représentées dans le modèle objet ADO.

Chaque objet peut être contenu dans sa collection correspondante. Un objet [Error](error-object-ado.md) peut, par exemple, être contenu dans une collection [Errors](errors-collection-ado.md). Pour plus d'informations, consultez [Collections ADO](ado-collections.md) ou une rubrique spécifique à une collection.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></p></td>
<td><p>Crée un objet <strong>Record</strong> ADO à partir d'un objet <strong>Row</strong> OLE DB dans une application C/C++.</p></td>
</tr>
<tr class="even">
<td><p><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></p></td>
<td><p>Crée un objet <strong>Recordset</strong> ADO à partir d'un objet <strong>Rowset</strong> OLE DB dans une application C/C++.</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Erreur</a></p></td>
<td><p>Contient des détails sur les erreurs d'accès aux données relatives à une seule opération impliquant le fournisseur.</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Field</a></p></td>
<td><p>Représente une colonne de données avec un type de données commun.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameter-object-ado.md">Paramètre</a></p></td>
<td><p>Représente un paramètre ou un argument associé à un objet <strong>Command</strong> basé sur une requête paramétrée ou sur une procédure stockée.</p></td>
</tr>
<tr class="even">
<td><p><a href="property-object-ado.md">Propriété</a></p></td>
<td><p>Représente une caractéristique dynamique d'un objet ADO défini par le fournisseur.</p></td>
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

