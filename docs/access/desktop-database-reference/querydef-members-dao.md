---
title: Membres de l’objet QueryDef (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 84f8be8360996eb209462347dc18b118cf460442
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937616"
---
# <a name="querydef-members-dao"></a>Membres de l’objet QueryDef (DAO)


**S’applique à**: Access 2013, Office 2013

Un objet QueryDef est une définition stockée d'une requête dans une base de données du moteur de base de données Microsoft Access.

## <a name="methods"></a>Méthodes

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="querydef-cancel-method-dao.md">Annuler</a></strong></p></td>
<td><p></p>

> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.


<p>Annule l'exécution d'un appel asynchrone de méthode en attente (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-close-method-dao.md">Close</a></strong></p></td>
<td><p>Ferme un objet <strong>QueryDef</strong> ouvert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>Exécute une instruction SQL au niveau de l'objet spécifié.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Crée un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong> et l'ajoute à la collection <strong>Recordsets</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propriétés

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Définit ou renvoie le nombre d'enregistrements extraits d'une source de données ODBC qui seront placés dans le cache local. Valeur <strong>Long</strong> en lecture-écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui fournit des informations sur la source de base de données dans une requête SQL directe. Type <strong>String</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Renvoie la date et l'heure auxquelles un objet a été créé (espaces de travail Microsoft Access uniquement). Valeur <strong>Variant</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-fields-property-dao.md">Champs</a></strong></p></td>
<td><p>Renvoie une collection <strong><a href="fields-collection-dao.md">Fields</a></strong> qui représente tous les objets <strong><a href="field-object-dao.md">Field</a></strong> stockés pour l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données <strong>Variant</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></p></td>
<td><p>Définit ou renvoie le nombre maximum d'enregistrements à renvoyer pour une requête sur une source de données ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></p></td>
<td><p>Indique le nombre de secondes d'attente avant que ne survienne une erreur d'expiration lors de l'exécution d'un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong> sur une base de données ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-parameters-property-dao.md">Paramètres</a></strong></p></td>
<td><p>Renvoie une collection <strong><a href="parameters-collection-dao.md">Parameters</a></strong> qui contient tous les objets <strong><a href="parameter-object-dao.md">Parameter</a></strong> de l'objet <strong>QueryDef</strong> spécifié. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></p></td>
<td><p></p>

> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.


<p>Définit ou renvoie une valeur qui indique si la requête doit être préparée sur le serveur comme procédure stockée temporaire à l'aide d'une fonction API <strong>SQLPrepare</strong> ODBC avant l'exécution, ou juste exécutée à l'aide de la fonction API <strong>SQLExecDirect</strong> ODBC (espaces de travail ODBCDirect uniquement). En lecture/écriture <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Renvoie le nombre d'enregistrements affectés par le dernier appel de la méthode <strong><a href="querydef-execute-method-dao.md">Execute</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></p></td>
<td><p>Définit ou renvoie une valeur indiquant si une requête SQL directe sur une base de données externe renvoie des enregistrements (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></p></td>
<td><p>Définit ou renvoie l'instruction SQL qui définit la requête exécutée par un objet <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p></p>

> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.


<p>Indique si l'exécution d'une opération asynchrone (c.-à-d. une méthode appelée avec l'option <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a>) est terminée (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-type-property-dao.md">Type</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. En lecture seule<strong>entier</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type <strong>Boolean</strong> en lecture seule.</p></td>
</tr>
</tbody>
</table>

