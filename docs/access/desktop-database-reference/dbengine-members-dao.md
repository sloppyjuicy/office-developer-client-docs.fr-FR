---
title: DBEngine, membres (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dee1030540944fc0be6bc8fb69004188c28c0c73
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920409"
---
# <a name="dbengine-members-dao"></a>DBEngine, membres (DAO)


**S’applique à**: Access 2013, Office 2013

L'objet DBEngine est l'objet de niveau supérieur dans le modèle objet DAO.

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
<td><p><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></p></td>
<td><p>Commence une nouvelle transaction. <strong>Database</strong> en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>Met fin à la transaction en cours et enregistre les modifications.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></p></td>
<td><p>Copie et compacte une base de données fermée et offre la possibilité d'en modifier la version, l'ordre de classement et le chiffrement. (Pour les espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></p></td>
<td><p>Crée un objet <strong><a href="database-object-dao.md">Database</a></strong>, enregistre la base de données sur le disque, et renvoie un objet <strong>Database</strong> ouvert (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></p></td>
<td><p>Crée un nouvel objet <strong><a href="workspace-object-dao.md">Workspace</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-idle-method-dao.md">Inactif</a></strong></p></td>
<td><p>Suspend le traitement des données, ce qui permet au moteur de base de données Microsoft Access de terminer les tâches en cours, telles que l'optimisation de la mémoire ou les expirations de délai des pages (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-openconnection-method-dao.md">Méthode OpenConnection</a></strong></p></td>
<td><p></p>

> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.


<p>Ouvre un objet <strong><a href="connection-object-dao.md">Connection</a></strong> dans une source de données ODBC (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Ouvre une base de données spécifiée et renvoie une référence à l'objet <strong><a href="database-object-dao.md">Database</a></strong> qui la représente.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></p></td>
<td><p>Entre les informations de connexion pour une source de données ODBC dans le Registre Windows. Le pilote ODBC a besoin des informations de connexion lorsque la source de données ODBC est ouverte au cours d'une session.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-rollback-method-dao.md">Rollback</a></strong></p></td>
<td><p>Met fin à transaction en cours et restaure les bases de données dans l'objet <strong>Workspace</strong> à l'état dans lequel elles se trouvaient au début de la transaction actuelle.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></p></td>
<td><p>Remplace temporairement les valeurs des clés du moteur de base de données Microsoft Access dans le registre Windows (espaces de travail Microsoft Access uniquement).</p></td>
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
<td><p><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></p></td>
<td><p>Définit le mot de passe servant à créer l'objet <strong>Workspace</strong> par défaut lors de son initialisation. Valeur de type <strong>String</strong> en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique le type d'espace de travail qui sera utilisé par le prochain objet <strong><a href="workspace-object-dao.md">Workspace</a></strong> créé.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></p></td>
<td><p>Définit le nom d'utilisateur servant à créer l'objet <strong>Workspace</strong> par défaut lors de son initialisation. Valeur de type <strong>String</strong> en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-errors-property-dao.md">Erreurs</a></strong></p></td>
<td><p>Renvoie une collection <strong>Errors</strong> qui contient tous les objets <strong>Error</strong> enregistrés pour l'objet spécifié. Valeur en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></p></td>
<td><p>Définit ou renvoie des informations sur la clé du Registre Windows contenant les valeurs relatives au moteur de base de données Microsoft Access (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Définit ou renvoie le nombre de secondes devant s'écouler avant l'apparition d'une erreur lorsque vous essayez de vous connecter à une base de données ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-version-property-dao.md">Version</a></strong></p></td>
<td><p>Renvoie la version de DAO en cours d'utilisation. Valeur de type <strong>String</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></p></td>
<td><p>Renvoie une collection <strong>Workspaces</strong> qui contient tous les objets <strong>Workspace</strong> actifs et non masqués. Valeur en lecture seule.</p></td>
</tr>
</tbody>
</table>

