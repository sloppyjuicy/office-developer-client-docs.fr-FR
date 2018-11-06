---
title: Méthode DBEngine.OpenConnection (DAO)
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
ms.openlocfilehash: 82f65862c9a1fbb1441c6bd5620d3bf4e86a5c32
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997888"
---
# <a name="dbengineopenconnection-method-dao"></a>Méthode DBEngine.OpenConnection (DAO)

**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . OpenConnection (***nom***, ***Options***, ***ReadOnly***, ***connecter***)

*expression* Variable qui représente un objet **DBEngine** .

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
<th><p>Name</p></th>
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>Chaîne</strong></p></td>
<td><p>Expression sous forme de chaîne. Reportez-vous à la section sous Notes.</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Définit différentes options pour la connexion, selon les indications dans les notes. En fonction de cette valeur, le gestionnaire de pilotes ODBC invite l'utilisateur à indiquer les informations de connexion comme le nom de la source de données (DSN), le nom d'utilisateur et le mot de passe.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p><strong>True</strong> si la connexion doit être ouverte pour un accès en lecture seule et <strong>False</strong> si la connexion doit être ouverte pour un accès en lecture/écriture (valeur par défaut).</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Une chaîne de connexion ODBC. Voir la propriété <strong><a href="connection-connect-property-dao.md">Connect</a></strong> pour des éléments spécifiques et la syntaxe de cette chaîne. Un ajoutant au début &quot;ODBC ; &quot; est requis.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Connection

## <a name="remarks"></a>Remarques

Utilisez la méthode **OpenConnection** pour définir une connexion à une source de données ODBC à partir d'un espace de travail ODBCDirect. La méthode **OpenConnection** est similaire à la méthode **OpenDatabase**, mais elle n'y est pas équivalente. La différence principale est que la méthode **OpenConnection** est disponible dans un espace de travail ODBCDirect.

Si vous spécifiez un nom de source de données (DSN) ODBC inscrit dans l’argument connecter, l’argument nom peut être n’importe quelle chaîne valide et fournit également la propriété **Name** de l’objet **Connection** . Si un DSN valide n’est pas inclus dans l’argument connecter, nom doit faire référence à un DSN ODBC valide, qui sera également la propriété **Name** . Si nom ni se connecter contient un DSN valid, le Gestionnaire de pilote ODBC peut avoir (via l’argument options) pour inviter l’utilisateur pour les informations de connexion nécessaires. Le nom DSN indiqué à l'invite fournit ensuite la propriété **Name**.

L'argument options détermine si l'utilisateur doit être invité à établir la connexion, définit à quel moment cela doit avoir lieu, et décide si la connexion doit être ouverte ou non en mode asynchrone. Vous pouvez utiliser l'une des constantes ci-après.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
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

