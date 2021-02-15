---
title: ConnectionString, propriété (ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3612652f3473c0794dbfe9be60f84ea2e3fee252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295708"
---
# <a name="connectionstring-property-ado"></a>ConnectionString, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique les informations utilisées pour se connecter à une source de données.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **String**.

## <a name="remarks"></a>Remarques

Utilisez la **propriété ConnectionString** pour spécifier une source de données en passant une chaîne de connexion détaillée contenant une série d’arguments  *=* instructions de valeur séparées par des points-virgules.

ADO prend en charge cinq arguments pour la propriété **ConnectionString**. Tous les autres arguments sont transmis directement au fournisseur sans aucun traitement par ADO. Les arguments pris en charge par ADO sont les suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Provider=</em></p></td>
<td><p>Spécifie le nom d'un fournisseur à utiliser pour la connexion.</p></td>
</tr>
<tr class="even">
<td><p><em>File Name=</em></p></td>
<td><p>Spécifie le nom d'un fichier spécifique au fournisseur (par exemple, un objet de source de données persistant) contenant des informations de connexion prédéfinies.</p></td>
</tr>
<tr class="odd">
<td><p><em>Remote Provider=</em></p></td>
<td><p>Spécifie le nom d'un fournisseur à utiliser pour les connexions côté client. (Remote Data Service uniquement.)</p></td>
</tr>
<tr class="even">
<td><p><em>Remote Server=</em></p></td>
<td><p>Spécifie le nom du chemin d'accès du serveur à utiliser lors de l'ouverture d'une connexion côté client (RDS uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><em>URL=</em></p></td>
<td><p>Spécifie la chaîne de connexion sous la forme d'une URL absolue identifiant une ressource, comme un fichier ou un répertoire.</p></td>
</tr>
</tbody>
</table>


Une fois que vous avez défini la propriété **ConnectionString** et ouvert l’objet [Connection](connection-object-ado.md), le fournisseur peut modifier le contenu de la propriété, par exemple, en mappant les noms d’arguments définis par ADO aux équivalents du fournisseur.

La propriété **ConnectionString** hérite automatiquement de la valeur utilisée pour l’argument *ConnectionString* de la méthode [Open](open-method-ado-connection.md) afin que vous puissiez remplacer la propriété **ConnectionString** actuelle lors de l’appel de la méthode **Open**.

Si vous spécifiez l'argument *File Name*, ADO charge le fournisseur associé. Dès lors, vous ne pouvez pas passer en même temps les arguments *Provider* et *File Name*.

La propriété **ConnectionString** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu'elle est ouverte.

Les doublons d'un argument dans la propriété **ConnectionString** ne sont pas pris en compte. C'est la dernière instance de l'argument qui est utilisée.

**Utilisation du service de données à distance** Lorsqu’elle est utilisée sur un objet **Connection** côté client, la **propriété ConnectionString** peut inclure uniquement les paramètres *Fournisseur* distant et *Serveur* distant.

