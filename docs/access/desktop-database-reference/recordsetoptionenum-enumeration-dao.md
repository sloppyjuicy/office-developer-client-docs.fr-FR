---
title: RecordsetOptionEnum, énumération (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9e2a69f6952feb892de736e7ff3c3ca94e9da64
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717278"
---
# <a name="recordsetoptionenum-enumeration-dao"></a>RecordsetOptionEnum, énumération (DAO)


**S’applique à**: Access 2013, Office 2013

Utilisée avec la méthode **OpenRecordset** pour spécifier les caractéristiques d'un nouvel objet **Recordset**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbAppendOnly</p></td>
<td><p>8</p></td>
<td><p>Autorise l'utilisateur à ajouter de nouveaux enregistrements à la feuille de réponse dynamique mais l'empêche de lire les enregistrements existants.</p></td>
</tr>
<tr class="even">
<td><p>dbConsistent</p></td>
<td><p>32</p></td>
<td><p>Applique les mises à jour aux champs qui n'affecteront pas d'autres champs de la feuille de réponse dynamique (jeu d'enregistrements de type feuille de réponse dynamique ou instantané uniquement).</p></td>
</tr>
<tr class="odd">
<td><p>dbDenyRead</p></td>
<td><p>2</p></td>
<td><p>Empêche d'autres utilisateurs de lire les enregistrements du jeu d'enregistrements (de type table uniquement).</p></td>
</tr>
<tr class="even">
<td><p>dbDenyWrite</p></td>
<td><p>1</p></td>
<td><p>Empêche d'autres utilisateurs de modifier les enregistrements du jeu d'enregistrements.</p></td>
</tr>
<tr class="odd">
<td><p>dbExecDirect</p></td>
<td><p>2048</p></td>
<td><p>Exécute la requête sans appeler d'abord la fonction ODBC SQLPrepare.</p></td>
</tr>
<tr class="even">
<td><p>dbFailOnError</p></td>
<td><p>128</p></td>
<td><p>Restaure les mises à jour si une erreur se produit.</p></td>
</tr>
<tr class="odd">
<td><p>dbForwardOnly</p></td>
<td><p>256</p></td>
<td><p>Crée un jeu d'enregistrements de type instantané à déplacement vers l'avant (jeu d'enregistrements de type instantané uniquement).</p></td>
</tr>
<tr class="even">
<td><p>dbInconsistent</p></td>
<td><p>16</p></td>
<td><p>Applique les mises à jour à tous les champs de la feuille de réponse dynamique, et ce même si d'autres enregistrements sont affectés (jeu d'enregistrements de type feuille de réponse dynamique ou instantané uniquement).</p></td>
</tr>
<tr class="odd">
<td><p>peut entraîner</p></td>
<td><p>4</p></td>
<td><p>Ouvre le jeu d'enregistrements en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p>dbRunAsync</p></td>
<td><p>1024</p></td>
<td><p>Exécute la requête de manière asynchrone.</p></td>
</tr>
<tr class="odd">
<td><p>dbSeeChanges</p></td>
<td><p>512</p></td>
<td><p>Génère une erreur d'exécution si un autre utilisateur change les données que vous êtes en train de modifier (jeu d'enregistrements de type feuille de réponse dynamique uniquement).</p></td>
</tr>
<tr class="even">
<td><p>dbSQLPassThrough</p></td>
<td><p>64</p></td>
<td><p>Envoie une instruction SQL à une base de données ODBC (jeu d'enregistrements de type instantané uniquement).</p></td>
</tr>
</tbody>
</table>

