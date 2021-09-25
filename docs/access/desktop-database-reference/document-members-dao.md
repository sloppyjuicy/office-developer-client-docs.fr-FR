---
title: Document members (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7fdfd95721d0c5c8d93a9a26185883c18227da73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581419"
---
# <a name="document-members-dao"></a>Document members (DAO)


**S’applique à** : Access 2013, Office 2013

Un objet Document inclut des informations sur une instance d'un objet. L'objet peut être une base de données, une table enregistrée, une requête ou une relation (bases de données de moteur de base de données Microsoft Access uniquement).

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
<td><p><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
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
<td><p><strong><a href="document-container-property-dao.md">Conteneur</a></strong></p></td>
<td><p>Renvoie le nom de l'objet <strong><a href="container-object-dao.md">Container</a></strong> auquel un objet <strong>Document</strong> appartient (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Renvoie la date et l'heure de création d'un objet. Valeur de type <strong>Variant</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données <strong>Variant</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="document-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie le nom de l'objet spécifié. En lecture seule <strong>chaîne</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="document-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
</tbody>
</table>

