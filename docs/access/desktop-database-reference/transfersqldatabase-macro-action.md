---
title: TransferSQLDatabase, action de macro
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ae05da3d07cc17f54584d11282721ac83f23ccd8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926541"
---
# <a name="transfersqldatabase-macro-action"></a>TransferSQLDatabase, action de macro


**S’applique à**: Access 2013, Office 2013

Dans un projet Access, l'action **TransférerBaseDeDonnéesSQL** permet de transférer une base de données Microsoft SQL Server 7.0 ou version ultérieure vers une autre base de données SQL Server 7.0 ou version ultérieure. Pour plus d’informations sur le transfert d’une base de données, voir la documentation SQL Server.


> [!NOTE]
> [!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.



## <a name="setting"></a>Valeur

L'action **TransférerBaseDeDonnéesSQL** utilise les arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Serveur</strong></p></td>
<td><p>Nom du serveur de base de données SQL Server 7.0, ou version ultérieure, vers lequel la copie est effectuée.</p></td>
</tr>
<tr class="even">
<td><p><strong>Database</strong></p></td>
<td><p>Nom de la nouvelle base de données créée sur le serveur de destination.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Utiliser une connexion approuvée</strong></p></td>
<td><p>Spécifie si ou pas il est une connexion approuvée à SQL Server. Si la valeur <strong>Oui</strong>, il existe une connexion approuvée et les arguments <strong>connexion</strong> et <strong>mot de passe</strong> ne sont pas requis. Si défini sur <strong>No</strong>, le <strong>nom de connexion</strong> et <strong>le mot de passe</strong> des arguments est requis. La valeur par défaut est <strong>Oui</strong>. Lorsque vous utilisez une connexion approuvée, la sécurité de SQL Server s’intègre à la sécurité du système d’exploitation Windows pour fournir une seule sur le réseau et la base de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>Connexion</strong></p></td>
<td><p>Identificateur de connexion au serveur de destination.</p></td>
</tr>
<tr class="odd">
<td><p><strong>MotDePasse</strong></p></td>
<td><p>Mot de passe de l’argument <strong>Connexion</strong>. Ce mot de passe est stocké sous forme de texte dans le projet Access, mais il est masqué durant l’opération de transfert de base de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>Transfert des données de copie</strong></p></td>
<td><p>Spécifie si les données doivent être incluses dans l’opération de transfert de base de données. Si la valeur sélectionnée est <strong>Oui</strong>, toutes les données seront incluses pour toutes les tables, ainsi que les structures de données, les propriétés étendues et les objets de base de données. Si la valeur sélectionnée est <strong>Non</strong>, aucune donnée des tables ne sera incluse. Seules la structure de la table et les propriétés étendues seront créées sur le serveur de destination, ainsi que les objets de base de données, à l’exception toutefois des schémas de bases de données. La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Aucune autre opération n'est autorisée lors du processus de transfert de base de données.

Par défaut, l'action **TransférerBaseDeDonnéesSQL** copie les données, les définitions de données, les objets de base de données et les propriétés étendues telles que les valeurs par défaut, les contraintes de texte et les valeurs de recherche.

Pour pouvoir transférer une base de données, les conditions suivantes doivent être réunies :

  - Vous devez être membre du rôle sysadmin sur le serveur de destination (aucun rôle spécifique n'est requis sur le serveur source).

<!-- end list -->

  - Le serveur SQL actif, connecté au projet Access et au serveur de destination vers lequel la base de données est transférée doit être un serveur SQL Server version 7.0 ou ultérieure.


> [!NOTE]
> <P>[!REMARQUE] Les serveurs liés ne sont pas transférés lors du transfert d'une base de données.</P>



Pour exécuter l'action **TransférerBaseDeDonnéesSQL** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **TransferSQLDatabase** de l'objet **DoCmd**.

