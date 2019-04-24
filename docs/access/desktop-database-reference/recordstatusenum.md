---
title: RecordStatusEnum (référence de base de données de bureau Access)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a83de7730224c5ecd5080c795d38cf2e9a3305a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309379"
---
# <a name="recordstatusenum"></a>RecordStatusEnum

**S’applique à** : Access 2013, Office 2013

Spécifie l'état d'un enregistrement en cas de mise à jour par lots et autres opérations globales de ce type.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adRecCanceled</strong></p></td>
<td><p>0x100</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé car l'opération a été annulée.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecCantRelease</strong></p></td>
<td><p>0x400</p></td>
<td><p>Indique que le nouvel enregistrement n'a pas été sauvegardé car l'enregistrement existant était verrouillé.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecConcurrencyViolation</strong></p></td>
<td><p>0x800</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé car une concurrence optimiste était en cours.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecDBDeleted</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Indique que l'enregistrement a déjà été supprimé de la source de données.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecDeleted</strong></p></td>
<td><p>0x4</p></td>
<td><p>Indique que l'enregistrement a été supprimé.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecIntegrityViolation</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé car l'utilisateur n'a pas respecté les contraintes d'intégrité.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecInvalid</strong></p></td>
<td><p>0x10</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé car son signet n'est pas valide.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMaxChangesExceeded</strong></p></td>
<td><p>0 x 2000</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé car il existait trop de modifications en attente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecModified</strong></p></td>
<td><p>0x2</p></td>
<td><p>Indique que l'enregistrement a été modifié.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecMultipleChanges</strong></p></td>
<td><p>0x40</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé car il aurait affecté plusieurs enregistrements.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecNew</strong></p></td>
<td><p>0x1</p></td>
<td><p>Indique qu'il s'agit d'un nouvel enregistrement.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecObjectOpen</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé en raison d'un conflit avec un objet de stockage ouvert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecOK</strong></p></td>
<td><p>0</p></td>
<td><p>Indique que l'enregistrement a été mis à jour avec succès.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecOutOfMemory</strong></p></td>
<td><p>0x8000</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé car l'ordinateur manque de mémoire.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecPendingChanges</strong></p></td>
<td><p>0x80</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé car il fait référence à une insertion en attente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecPermissionDenied</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé car l'utilisateur ne dispose pas des autorisations suffisantes.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRecSchemaViolation</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Indique que l'enregistrement n'a pas été sauvegardé car il ne respecte pas la structure de la base de données sous-jacente.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecUnmodified</strong></p></td>
<td><p>0x8</p></td>
<td><p>Indique que l'enregistrement n'a pas été modifié.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

AdoEnums. RecordStatus.

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. RecordStatus. CANCELed</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. RecordStatus. CANTRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. RecordStatus. CONCURRENCYVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. RecordStatus. DBDELETED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. RecordStatus. DELETEd</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. RecordStatus. INTEGRITYVIOLATION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. RecordStatus. inVALID</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. RecordStatus. MAXCHANGESEXCEEDED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. RecordStatus. MODIFIEd</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. RecordStatus. MULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. RecordStatus. NEW</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. RecordStatus. OBJETOPEN,</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. RecordStatus. OK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. RecordStatus. OUTOFMEMORY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. RecordStatus. PENDINGCHANGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. RecordStatus. PERMISSIONDENIED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. RecordStatus. SCHEMAVIOLATION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. RecordStatus. unMODIFIEd</p></td>
</tr>
</tbody>
</table>

