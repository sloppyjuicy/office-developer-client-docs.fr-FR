---
title: DBEngine.OpenConnection, méthode (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 778a581f-be42-94ee-e5c6-4cbc1843450d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196074(v=office.15)
ms:contentKeyID: 48545729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053574
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 61014716b78af9cbfcd2b7c24e131cbd63c89095
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597456"
---
# <a name="dbengineopenconnection-method-dao"></a>DBEngine.OpenConnection, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*.* OpenConnection(***Name** _, _*_Options_*_, _*_ReadOnly_*_, _*_Connecter_**)

*expression* Variable représentant un objet **DBEngine**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Expression sous forme de chaîne. Reportez-vous à la section sous Notes.</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Définit différentes options pour la connexion, selon les indications dans les notes. En fonction de cette valeur, le gestionnaire de pilotes ODBC invite l'utilisateur à indiquer les informations de connexion comme le nom de la source de données (DSN), le nom d'utilisateur et le mot de passe.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> si la connexion doit être ouverte pour un accès en lecture seule et <strong>False</strong> si la connexion doit être ouverte pour un accès en lecture/écriture (valeur par défaut).</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Chaîne de connexion ODBC. Voir la <strong><a href="connection-connect-property-dao.md">propriété Connecter</a></strong> pour les éléments et la syntaxe spécifiques de cette chaîne. OdBC prédépendant &quot; &quot; est requis.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Connection

## <a name="remarks"></a>Remarques

Utilisez la méthode **OpenConnection** pour définir une connexion à une source de données ODBC à partir d'un espace de travail ODBCDirect. La méthode **OpenConnection** est similaire à la méthode **OpenDatabase**, mais elle n'y est pas équivalente. La différence principale est que la méthode **OpenConnection** est disponible dans un espace de travail ODBCDirect.

Si vous spécifiez un nom de source de données ODBC enregistré dans l’argument de connexion, l’argument nom peut être n’importe quelle chaîne valide et fournit également la propriété **Name** de l’objet **Connection.** Si aucun nom DSN valide n’est inclus dans l’argument de connexion, le nom doit faire référence à un nom DSN ODBC valide, qui sera également la propriété **Name.** Si ni le nom ni la connexion ne contiennent un nom DSN valide, le gestionnaire de pilotes ODBC peut être définie (via l’argument Options) pour inviter l’utilisateur à fournir les informations de connexion requises. Le nom DSN indiqué à l'invite fournit ensuite la propriété **Name**.

L’argument Options détermine si et quand demander à l’utilisateur d’établir la connexion, et s’il faut ou non ouvrir la connexion de manière asynchrone. Vous pouvez utiliser l'une des constantes ci-après.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDriverNoPrompt</strong></p></td>
<td><p>Le gestionnaire de pilotes ODBC utilise la chaîne de connexion fournie dans <em>dbname</em> et <em>connect</em>. Si vous ne fournissez pas suffisamment d’informations, une erreur d’exécution se produit.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverPrompt</strong></p></td>
<td><p>Le gestionnaire de pilotes ODBC affiche la boîte de dialogue <strong>Sources de données ODBC</strong>, qui affiche les informations pertinentes fournies dans <em>dbname</em> ou <em>connect</em>. La chaîne de connexion est composée du DSN que l'utilisateur sélectionné par le biais des boîtes de dialogue, ou, si l'utilisateur ne spécifie pas de DSN, c'est le DSN par défaut qui est utilisé.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDriverComplete</strong></p></td>
<td><p>Valeur par défaut. Si l'argument <em>connect</em> inclut toutes les informations nécessaires pour établir une connexion, le gestionnaire de pilotes ODBC utilise la chaîne dans <em>connect</em>. Autrement, il se comporte comme lorsque vous spécifiez <strong>dbDriverPrompt</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverCompleteRequired</strong></p></td>
<td><p>Cette option se comporte comme <strong>dbDriverComplete</strong> sauf que le pilote ODBC désactive les invites pour les informations qui ne sont pas nécessaires à l'établissement de la connexion.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Exécute la méthode en mode asynchrone. Cette constante peut être utilisée avec n'importe quelles autres constantes <em>options</em>.</p></td>
</tr>
</tbody>
</table>


**OpenConnection** renvoie un objet **Connection** qui contient des informations sur la connexion. L'objet **Connection** est similaire à un objet **[Database](database-object-dao.md)**. La différence principale réside dans le fait qu'un objet **Database** représente généralement une base de données, même s'il peut être utilisé pour représenter une connexion à une source de données ODBC issue d'un espace de travail Microsoft Access.

