---
title: DBEngine.OpenConnection Method (DAO)
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
ms.openlocfilehash: 3110bd89b0dc56b13a42c7152465c0f9b39e3175
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607045"
---
# <a name="dbengineopenconnection-method-dao"></a><span data-ttu-id="f739f-102">DBEngine.OpenConnection Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="f739f-102">DBEngine.OpenConnection Method (DAO)</span></span>


<span data-ttu-id="f739f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f739f-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="f739f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f739f-104">Syntax</span></span>

<span data-ttu-id="f739f-105">*expression* . OpenConnection (***nom***, ***Options***, ***ReadOnly***, ***connecter***)</span><span class="sxs-lookup"><span data-stu-id="f739f-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="f739f-106">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="f739f-106">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="f739f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f739f-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f739f-108">Name</span><span class="sxs-lookup"><span data-stu-id="f739f-108">Name</span></span></p></th>
<th><p><span data-ttu-id="f739f-109">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="f739f-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f739f-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="f739f-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="f739f-111">Description</span><span class="sxs-lookup"><span data-stu-id="f739f-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f739f-112">Name</span><span class="sxs-lookup"><span data-stu-id="f739f-112">Name</span></span></p></td>
<td><p><span data-ttu-id="f739f-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f739f-113">Required</span></span></p></td>
<td><p><span data-ttu-id="f739f-114"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="f739f-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f739f-p101">Expression sous forme de chaîne. Reportez-vous à la section sous Notes.</span><span class="sxs-lookup"><span data-stu-id="f739f-p101">A string expression. See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f739f-117">Options</span><span class="sxs-lookup"><span data-stu-id="f739f-117">Options</span></span></p></td>
<td><p><span data-ttu-id="f739f-118">Facultatif</span><span class="sxs-lookup"><span data-stu-id="f739f-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="f739f-119"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="f739f-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f739f-p102">Définit différentes options pour la connexion, selon les indications dans les notes. En fonction de cette valeur, le gestionnaire de pilotes ODBC invite l'utilisateur à indiquer les informations de connexion comme le nom de la source de données (DSN), le nom d'utilisateur et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f739f-p102">sets various options for the connection, as specified in Remarks. Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f739f-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f739f-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="f739f-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="f739f-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="f739f-124"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="f739f-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f739f-125"><strong>True</strong> si la connexion doit être ouverte pour un accès en lecture seule et <strong>False</strong> si la connexion doit être ouverte pour un accès en lecture/écriture (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="f739f-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f739f-126">Connexion</span><span class="sxs-lookup"><span data-stu-id="f739f-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="f739f-127">Facultatif</span><span class="sxs-lookup"><span data-stu-id="f739f-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="f739f-128"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="f739f-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f739f-129">Une chaîne de connexion ODBC.</span><span class="sxs-lookup"><span data-stu-id="f739f-129">An ODBC connection string.</span></span> <span data-ttu-id="f739f-130">Voir la propriété <strong><a href="connection-connect-property-dao.md">Connect</a></strong> pour des éléments spécifiques et la syntaxe de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="f739f-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="f739f-131">Un ajoutant au début &quot;ODBC ; &quot; est requis.</span><span class="sxs-lookup"><span data-stu-id="f739f-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f739f-132"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="f739f-132"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="f739f-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f739f-133">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="f739f-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f739f-134">Return value</span></span>
>>>>>>> <span data-ttu-id="f739f-135">master</span><span class="sxs-lookup"><span data-stu-id="f739f-135">master</span></span>

<span data-ttu-id="f739f-136">Connection</span><span class="sxs-lookup"><span data-stu-id="f739f-136">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="f739f-137">Remarques</span><span class="sxs-lookup"><span data-stu-id="f739f-137">Remarks</span></span>

<span data-ttu-id="f739f-p104">Utilisez la méthode **OpenConnection** pour définir une connexion à une source de données ODBC à partir d'un espace de travail ODBCDirect. La méthode **OpenConnection** est similaire à la méthode **OpenDatabase**, mais elle n'y est pas équivalente. La différence principale est que la méthode **OpenConnection** est disponible dans un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="f739f-p104">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace. The **OpenConnection** method is similar but not equivalent to **OpenDatabase**. The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="f739f-141">Si vous spécifiez un nom de source de données (DSN) ODBC inscrit dans l’argument connecter, l’argument nom peut être n’importe quelle chaîne valide et fournit également la propriété **Name** de l’objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="f739f-141">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="f739f-142">Si un DSN valide n’est pas inclus dans l’argument connecter, nom doit faire référence à un DSN ODBC valide, qui sera également la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="f739f-142">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="f739f-143">Si nom ni se connecter contient un DSN valid, le Gestionnaire de pilote ODBC peut avoir (via l’argument options) pour inviter l’utilisateur pour les informations de connexion nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f739f-143">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="f739f-144">Le nom DSN indiqué à l'invite fournit ensuite la propriété **Name**.</span><span class="sxs-lookup"><span data-stu-id="f739f-144">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="f739f-p106">L'argument options détermine si l'utilisateur doit être invité à établir la connexion, définit à quel moment cela doit avoir lieu, et décide si la connexion doit être ouverte ou non en mode asynchrone. Vous pouvez utiliser l'une des constantes ci-après.</span><span class="sxs-lookup"><span data-stu-id="f739f-p106">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously. You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f739f-147">Constant</span><span class="sxs-lookup"><span data-stu-id="f739f-147">Constant</span></span></p></th>
<th><p><span data-ttu-id="f739f-148">Description</span><span class="sxs-lookup"><span data-stu-id="f739f-148">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f739f-149"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="f739f-149"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="f739f-p107">Le gestionnaire de pilotes ODBC utilise la chaîne de connexion fournie dans <em>dbname</em> et <em>connect</em>. Si vous ne fournissez pas suffisamment d’informations, une erreur d’exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="f739f-p107">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>. If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f739f-152"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="f739f-152"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="f739f-p108">Le gestionnaire de pilotes ODBC affiche la boîte de dialogue <strong>Sources de données ODBC</strong>, qui affiche les informations pertinentes fournies dans <em>dbname</em> ou <em>connect</em>. La chaîne de connexion est composée du DSN que l'utilisateur sélectionné par le biais des boîtes de dialogue, ou, si l'utilisateur ne spécifie pas de DSN, c'est le DSN par défaut qui est utilisé.</span><span class="sxs-lookup"><span data-stu-id="f739f-p108">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>. The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f739f-155"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="f739f-155"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="f739f-p109">Valeur par défaut. Si l'argument <em>connect</em> inclut toutes les informations nécessaires pour établir une connexion, le gestionnaire de pilotes ODBC utilise la chaîne dans <em>connect</em>. Autrement, il se comporte comme lorsque vous spécifiez <strong>dbDriverPrompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="f739f-p109">Default. If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>. Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f739f-159"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="f739f-159"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="f739f-160">Cette option se comporte comme <strong>dbDriverComplete</strong> sauf que le pilote ODBC désactive les invites pour les informations qui ne sont pas nécessaires à l'établissement de la connexion.</span><span class="sxs-lookup"><span data-stu-id="f739f-160">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f739f-161"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="f739f-161"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="f739f-p110">Exécute la méthode en mode asynchrone. Cette constante peut être utilisée avec n'importe quelles autres constantes <em>options</em>.</span><span class="sxs-lookup"><span data-stu-id="f739f-p110">Execute the method asynchronously. This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f739f-p111">**OpenConnection** renvoie un objet **Connection** qui contient des informations sur la connexion. L'objet **Connection** est similaire à un objet **[Database](database-object-dao.md)**. La différence principale réside dans le fait qu'un objet **Database** représente généralement une base de données, même s'il peut être utilisé pour représenter une connexion à une source de données ODBC issue d'un espace de travail Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f739f-p111">**OpenConnection** returns a **Connection** object which contains information about the connection. The **Connection** object is similar to a **[Database](database-object-dao.md)** object. The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

