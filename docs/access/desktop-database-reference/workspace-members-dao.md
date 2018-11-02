---
title: Membres de l’espace de travail (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f3deb259e5058fe595099e5fa556ff5fca8e4baf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923888"
---
# <a name="workspace-members-dao"></a>Membres de l’espace de travail (DAO)


**S’applique à**: Access 2013, Office 2013

Un objet Workspace définit une session nommée pour un utilisateur. Il contient des bases de données ouvertes et fournit les mécanismes destinés aux transactions simultanées, ainsi que la prise en charge des groupes de travail sécurisés dans les espaces de travail Microsoft Access.

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
<td><p><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></p></td>
<td><p>Commence une nouvelle transaction. <strong>Database</strong> en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-close-method-dao.md">Close</a></strong></p></td>
<td><p>Ferme un objet <strong>Workspace</strong> ouvert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>Met fin à la transaction en cours et enregistre les modifications.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></p></td>
<td><p>Crée un objet <strong><a href="database-object-dao.md">Database</a></strong>, enregistre la base de données sur le disque, et renvoie un objet <strong>Database</strong> ouvert (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-openconnection-method-dao.md">Méthode OpenConnection</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</P>


<p>Ouvre un objet <strong><a href="connection-object-dao.md">Connection</a></strong> dans une source de données ODBC (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Ouvre une base de données spécifiée dans un objet <strong><a href="workspace-object-dao.md">Workspace</a></strong> et renvoie une référence à l'objet <strong><a href="database-object-dao.md">Database</a></strong> qui le représente.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></p></td>
<td><p>Met fin à transaction en cours et restaure les bases de données dans l'objet <strong>Workspace</strong> à l'état dans lequel elles se trouvaient au début de la transaction actuelle.</p></td>
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
<td><p><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></p></td>
<td><p>Renvoie une collection <strong>Connections</strong> qui représente les connexions actives dans l'objet <strong>Workspace</strong> spécifié. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></p></td>
<td><p>Renvoie une collection <strong>Databases</strong> qui représente les bases de données ouvertes dans l'objet <strong>Workspace</strong> spécifié. En lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</P>


<p>Définit ou renvoie le type de pilote de curseur utilisé pour la connexion créée par la méthode <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> ou <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si plusieurs transactions impliquant la même source de données ODBC connectée au moteur de base de données Microsoft Access sont isolées (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Définit ou renvoie le nombre de secondes devant s'écouler avant l'apparition d'une erreur lorsque vous essayez de vous connecter à une base de données ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-type-property-dao.md">Type</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données <strong>Integer</strong> en lecture seule.</p></td>
</tr>
</tbody>
</table>

