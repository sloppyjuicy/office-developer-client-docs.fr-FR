---
title: DBEngine. OpenConnection, méthode (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 845c710954d83003f49a6cd9db21ae3f3bfab383
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294259"
---
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="63bff-102">DBEngine. OpenConnection, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="63bff-102">DBEngine.OpenConnection method (DAO)</span></span>

<span data-ttu-id="63bff-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63bff-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="63bff-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63bff-104">Syntax</span></span>

<span data-ttu-id="63bff-105">*expression* . OpenConnection (***nom***, ***options***, ***LectureSeule***, ***connexion***)</span><span class="sxs-lookup"><span data-stu-id="63bff-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="63bff-106">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="63bff-106">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="63bff-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63bff-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63bff-108">Nom</span><span class="sxs-lookup"><span data-stu-id="63bff-108">Name</span></span></p></th>
<th><p><span data-ttu-id="63bff-109">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="63bff-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="63bff-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="63bff-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="63bff-111">Description</span><span class="sxs-lookup"><span data-stu-id="63bff-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63bff-112"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="63bff-112"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="63bff-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="63bff-113">Required</span></span></p></td>
<td><p><span data-ttu-id="63bff-114"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="63bff-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="63bff-115">Expression sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="63bff-115">A string expression.</span></span> <span data-ttu-id="63bff-116">Reportez-vous à la section sous Notes.</span><span class="sxs-lookup"><span data-stu-id="63bff-116">See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63bff-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="63bff-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="63bff-118">Facultatif</span><span class="sxs-lookup"><span data-stu-id="63bff-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="63bff-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="63bff-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="63bff-p102">Définit différentes options pour la connexion, selon les indications dans les notes. En fonction de cette valeur, le gestionnaire de pilotes ODBC invite l'utilisateur à indiquer les informations de connexion comme le nom de la source de données (DSN), le nom d'utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="63bff-p102">sets various options for the connection, as specified in Remarks. Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63bff-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="63bff-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="63bff-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="63bff-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="63bff-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="63bff-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="63bff-125"><strong>True</strong> si la connexion doit être ouverte pour un accès en lecture seule et <strong>False</strong> si la connexion doit être ouverte pour un accès en lecture/écriture (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="63bff-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63bff-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="63bff-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="63bff-127">Facultatif</span><span class="sxs-lookup"><span data-stu-id="63bff-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="63bff-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="63bff-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="63bff-129">Chaîne de connexion ODBC.</span><span class="sxs-lookup"><span data-stu-id="63bff-129">An ODBC connection string.</span></span> <span data-ttu-id="63bff-130">Voir la propriété <strong><a href="connection-connect-property-dao.md">Connect</a></strong> pour les éléments et la syntaxe spécifiques de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="63bff-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="63bff-131">Un ODBC &quot;ajouté; &quot; est requis.</span><span class="sxs-lookup"><span data-stu-id="63bff-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="63bff-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="63bff-132">Return value</span></span>

<span data-ttu-id="63bff-133">Connection</span><span class="sxs-lookup"><span data-stu-id="63bff-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="63bff-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="63bff-134">Remarks</span></span>

<span data-ttu-id="63bff-p104">Utilisez la méthode **OpenConnection** pour définir une connexion à une source de données ODBC à partir d'un espace de travail ODBCDirect. La méthode **OpenConnection** est similaire à la méthode **OpenDatabase**, mais elle n'y est pas équivalente. La différence principale est que la méthode **OpenConnection** est disponible dans un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="63bff-p104">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace. The **OpenConnection** method is similar but not equivalent to **OpenDatabase**. The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="63bff-138">Si vous spécifiez un nom de source de données (DSN) ODBC enregistré dans l'argument connecter, l'argument nom peut être n'importe quelle chaîne valide et fournira également la propriété **Name** de l'objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="63bff-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="63bff-139">Si un DSN valide n'est pas inclus dans l'argument Connect, le nom doit faire référence à un DSN ODBC valide, qui sera également la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="63bff-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="63bff-140">Si ni le nom ni la connexion ne contiennent un DSN valide, le gestionnaire de pilotes ODBC peut être défini (via l'argument options) pour inviter l'utilisateur à entrer les informations de connexion requises.</span><span class="sxs-lookup"><span data-stu-id="63bff-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="63bff-141">Le nom DSN indiqué à l'invite fournit ensuite la propriété **Name**.</span><span class="sxs-lookup"><span data-stu-id="63bff-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="63bff-142">L'argument options détermine si et quand demander à l'utilisateur d'établir la connexion, et s'il faut ou non l'ouvrir de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="63bff-142">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously.</span></span> <span data-ttu-id="63bff-143">Vous pouvez utiliser l'une des constantes ci-après.</span><span class="sxs-lookup"><span data-stu-id="63bff-143">You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63bff-144">Constante</span><span class="sxs-lookup"><span data-stu-id="63bff-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="63bff-145">Description</span><span class="sxs-lookup"><span data-stu-id="63bff-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63bff-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="63bff-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="63bff-147">Le gestionnaire de pilotes ODBC utilise la chaîne de connexion fournie dans <em>dbname</em> et <em>connect</em>.</span><span class="sxs-lookup"><span data-stu-id="63bff-147">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>.</span></span> <span data-ttu-id="63bff-148">Si vous ne fournissez pas suffisamment d’informations, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="63bff-148">If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63bff-149"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="63bff-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="63bff-p108">Le gestionnaire de pilotes ODBC affiche la boîte de dialogue <strong>Sources de données ODBC</strong>, qui affiche les informations pertinentes fournies dans <em>dbname</em> ou <em>connect</em>. La chaîne de connexion est composée du DSN que l'utilisateur sélectionné par le biais des boîtes de dialogue, ou, si l'utilisateur ne spécifie pas de DSN, c'est le DSN par défaut qui est utilisé.</span><span class="sxs-lookup"><span data-stu-id="63bff-p108">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>. The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63bff-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="63bff-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="63bff-p109">Valeur par défaut. Si l'argument <em>connect</em> inclut toutes les informations nécessaires pour établir une connexion, le gestionnaire de pilotes ODBC utilise la chaîne dans <em>connect</em>. Autrement, il se comporte comme lorsque vous spécifiez <strong>dbDriverPrompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="63bff-p109">Default. If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>. Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63bff-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="63bff-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="63bff-157">Cette option se comporte comme <strong>dbDriverComplete</strong> sauf que le pilote ODBC désactive les invites pour les informations qui ne sont pas nécessaires à l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="63bff-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63bff-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="63bff-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="63bff-159">Exécute la méthode en mode asynchrone.</span><span class="sxs-lookup"><span data-stu-id="63bff-159">Execute the method asynchronously.</span></span> <span data-ttu-id="63bff-160">Cette constante peut être utilisée avec n'importe quelles autres constantes <em>options</em>.</span><span class="sxs-lookup"><span data-stu-id="63bff-160">This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="63bff-p111">**OpenConnection** renvoie un objet **Connection** qui contient des informations sur la connexion. L'objet **Connection** est similaire à un objet **[Database](database-object-dao.md)**. La différence principale réside dans le fait qu'un objet **Database** représente généralement une base de données, même s'il peut être utilisé pour représenter une connexion à une source de données ODBC issue d'un espace de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="63bff-p111">**OpenConnection** returns a **Connection** object which contains information about the connection. The **Connection** object is similar to a **[Database](database-object-dao.md)** object. The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

