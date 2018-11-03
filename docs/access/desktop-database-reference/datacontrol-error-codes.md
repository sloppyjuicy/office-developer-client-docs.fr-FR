---
title: Codes d’erreur DataControl
TOCTitle: DataControl error codes
ms:assetid: d81446e2-aae6-b460-08a3-eae9920dc767
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250089(v=office.15)
ms:contentKeyID: 48548027
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fcb9a2cd456e09edc84475fb47c5cca8a548d561
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947762"
---
# <a name="datacontrol-error-codes"></a>Codes d’erreur DataControl


**S’applique à**: Access 2013, Office 2013

Le tableau suivant répertorie les codes d'erreur de l'objet [RDS.DataControl](datacontrol-object-rds.md). Il affiche la traduction décimale positive des deux octets bas, la traduction décimale négative du code d'erreur complet et les valeurs hexadécimales.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Erreurs RDS.DataControl</p></th>
<th><p>Code</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>IDS_AsyncPending</strong></p></td>
<td><p>4107<br />
-2146824175<br />
0x800A1011</p></td>
<td><p>Impossible d'exécuter l'opération avec une opération asynchrone en attente.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_BadInlineTablegram</strong></p></td>
<td><p>4105<br />
-2146824183<br />
0x800A1009</p></td>
<td><p>Tablegram incorrect.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CantConnect</strong></p></td>
<td><p>4099<br />
-2146824189<br />
0x800A1003</p></td>
<td><p>Impossible de se connecter au serveur.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_CantCreateObject</strong></p></td>
<td><p>4100<br />
-2146824188<br />
0x800A1004</p></td>
<td><p>Impossible de créer un objet Business.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CantFindDataspace</strong></p></td>
<td><p>4102<br />
-2146824186<br />
0x800A1006</p></td>
<td><p>La propriété Dataspace n'est pas valide.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_CantInvokeMethod</strong></p></td>
<td><p>4101<br />
-2146824187<br />
0x800A1005</p></td>
<td><p>Impossible d'invoquer une méthode sur l'objet Business.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CrossDomainWarning</strong></p></td>
<td><p>4112<br />
-2146824170<br />
0x800A1016</p></td>
<td><p>Cette page accède aux données sur un autre domaine. Vous souhaitez autoriser cela ? Pour éviter ce message dans Internet Explorer, vous pouvez ajouter un site Web sécurisé à la zone Sites de confiance sur l’onglet <strong>sécurité</strong> de la boîte de dialogue <strong>Options Internet</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_InvalidADCClientVersion</strong></p></td>
<td><p>4106<br />
-2146824176<br />
0x800A1010</p></td>
<td><p>Version du Client RDS non valide — Le Client est plus récente que celle du serveur.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_INVALIDARG</strong></p></td>
<td><p>5376<br />
-2147019520<br />
0x80071500</p></td>
<td><p>Un ou plusieurs arguments ne sont pas valides.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_InvalidBindings</strong></p></td>
<td><p>4097<br />
-2146824191<br />
0x800A1001</p></td>
<td><p>Erreur dans la propriété bindings.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_InvalidParam</strong></p></td>
<td><p>4110<br />
-2146824172<br />
0x800A1014</p></td>
<td><p>Un ou plusieurs arguments ne sont pas valides.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_NOINTERFACE</strong></p></td>
<td><p>5377<br />
-2147019519<br />
0x80071501</p></td>
<td><p>Ce type d'interface n'est pas pris en charge.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_NotReentrant</strong></p></td>
<td><p>4111<br />
-2146824171<br />
0x800A1015</p></td>
<td><p>La requête ne peut pas être exécutée pendant que le gestionnaire d'événements est en cours de traitement.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_ObjectNotSafe</strong></p></td>
<td><p>4103<br />
-2146824185<br />
0x800A1007</p></td>
<td><p>Les paramètres de sécurité définis sur cette machine interdisent la création d'un objet Business.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_RecordsetNotOpen</strong></p></td>
<td><p>4109<br />
-2146824173<br />
0x800A1013</p></td>
<td><p>Le <strong>jeu d'enregistrements</strong> n'est pas ouvert.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_ResetInvalidField</strong></p></td>
<td><p>4108<br />
-2146824174<br />
0x800A1012</p></td>
<td><p>La colonne spécifiée dans  <strong>SortColumn</strong> ou <strong>FilterColumn</strong> n'existe pas.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_RowsetNotUpdateable</strong></p></td>
<td><p>4104<br />
-2146824184<br />
0x800A1008</p></td>
<td><p>Impossible de mettre à jour l'ensemble de lignes.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_UnexpectedError</strong></p></td>
<td><p>4351<br />
-2146823937<br />
0x800A10FF</p></td>
<td><p>Erreur inattendue.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_UpdatesFailed</strong></p></td>
<td><p>4098<br />
-2146824190<br />
0x800A1002</p></td>
<td><p>Impossible de mettre à jour la base de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_URLMONNotFound</strong></p></td>
<td><p>4119<br />
-2146824169<br />
0x800A1017</p></td>
<td><p>La propriété <strong>URL</strong> du DataControl nécessite le fichier système Urlmon.dll, qui est introuvable.</p></td>
</tr>
</tbody>
</table>

