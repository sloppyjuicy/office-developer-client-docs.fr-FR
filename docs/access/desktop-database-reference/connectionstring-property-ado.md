---
title: ConnectionString, propriété (ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 48e8998676a9c96bc7a6820d765a8b17a9dfafef
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882797"
---
# <a name="connectionstring-property-ado"></a>ConnectionString, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique les informations utilisées pour se connecter à une source de données.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **String**.

## <a name="remarks"></a>Notes

Utilisez la propriété **ConnectionString** pour spécifier une source de données en passant une chaîne de connexion détaillée contenant une série d’instructions *argument* *= valeur* , séparées par des points-virgules.

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
<td><p><em>Nom de fichier =</em></p></td>
<td><p>Spécifie le nom d'un fichier spécifique au fournisseur (par exemple, un objet de source de données persistant) contenant des informations de connexion prédéfinies.</p></td>
</tr>
<tr class="odd">
<td><p><em>Fournisseur distant =</em></p></td>
<td><p>Spécifie le nom d'un fournisseur à utiliser lors de l'ouverture d'une connexion côté client (RDS uniquement).</p></td>
</tr>
<tr class="even">
<td><p><em>Serveur distant =</em></p></td>
<td><p>Spécifie le nom du chemin d'accès du serveur à utiliser lors de l'ouverture d'une connexion côté client (RDS uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><em>URL=</em></p></td>
<td><p>Spécifie la chaîne de connexion sous la forme d'une URL absolue identifiant une ressource, comme un fichier ou un répertoire.</p></td>
</tr>
</tbody>
</table>


Une fois que vous avez défini la propriété **ConnectionString** et ouvert l'objet [Connection](connection-object-ado.md), le fournisseur peut modifier le contenu de la propriété, par exemple, en mappant les noms d'arguments définis par ADO aux équivalents du fournisseur.

La propriété **ConnectionString** hérite automatiquement de la valeur utilisée pour l’argument *ConnectionString* de la méthode [Open](open-method-ado-connection.md) , afin que vous pouvez remplacer la propriété **ConnectionString** actuelle lors de l’appel de méthode **Open** .

Étant donné que l’argument *Nom de fichier* , ADO charge le fournisseur associé, vous ne peuvent pas passer des arguments à la fois le *fournisseur* et le *Nom de fichier* .

La propriété **ConnectionString** est en lecture/écriture lorsque la connexion est fermée et en lecture seule lorsqu'elle est ouverte.

Les doublons d'un argument dans la propriété **ConnectionString** ne sont pas pris en compte. C'est la dernière instance de l'argument qui est utilisée.

**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet de **connexion** côté client, la propriété **ConnectionString** peut inclure que les paramètres *Remote Provider* et *Remote Server* .

