---
title: Connection.Execute method (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8140dbe9bc0c68d467c011d77bc0c00cec7ad560
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295911"
---
# <a name="connectionexecute-method-dao"></a><span data-ttu-id="1abd9-102">Connection.Execute method (DAO)</span><span class="sxs-lookup"><span data-stu-id="1abd9-102">Connection.Execute method (DAO)</span></span>

<span data-ttu-id="1abd9-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1abd9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1abd9-104">Exécute une requête action ou exécute une instruction SQL sur l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="1abd9-104">Runs an action query or executes an SQL statement on the specified object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1abd9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1abd9-105">Syntax</span></span>

<span data-ttu-id="1abd9-106">*expression* .Execute(***Query***, ***Options***)</span><span class="sxs-lookup"><span data-stu-id="1abd9-106">*expression* .Execute(***Query***, ***Options***)</span></span>

<span data-ttu-id="1abd9-107">*expression* Variable qui représente un objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="1abd9-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1abd9-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="1abd9-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1abd9-109">Nom</span><span class="sxs-lookup"><span data-stu-id="1abd9-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1abd9-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="1abd9-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1abd9-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="1abd9-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1abd9-112">Description</span><span class="sxs-lookup"><span data-stu-id="1abd9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1abd9-113"><em>Query</em></span><span class="sxs-lookup"><span data-stu-id="1abd9-113"><em>Query</em></span></span></p></td>
<td><p><span data-ttu-id="1abd9-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1abd9-114">Required</span></span></p></td>
<td><p><span data-ttu-id="1abd9-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1abd9-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1abd9-116">Type <strong>String</strong> qui représente une instruction SQL ou la valeur de la propriété <strong>Name</strong> d'un objet <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="1abd9-116">A <strong>String</strong> that is an SQL statement or the <strong>Name</strong> property value of a <strong>QueryDef</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1abd9-117"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="1abd9-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="1abd9-118">Facultatif</span><span class="sxs-lookup"><span data-stu-id="1abd9-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="1abd9-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1abd9-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1abd9-120">Constante ou combinaison de constantes déterminant les caractéristiques d'intégrité des données de la requêtes, comme indiqué dans la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="1abd9-120">A constant or combination of constants that determines the data integrity characteristics of the query, as specified in Settings.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1abd9-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="1abd9-121">Remarks</span></span>

<span data-ttu-id="1abd9-122">Vous pouvez utiliser les constantes **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** suivantes comme options.</span><span class="sxs-lookup"><span data-stu-id="1abd9-122">You can use the following **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** constants for options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1abd9-123">Constante</span><span class="sxs-lookup"><span data-stu-id="1abd9-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="1abd9-124">Description</span><span class="sxs-lookup"><span data-stu-id="1abd9-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1abd9-125"><strong>dbDenyWrite</strong></span><span class="sxs-lookup"><span data-stu-id="1abd9-125"><strong>dbDenyWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="1abd9-126">Refuse les autorisations d’accès en écriture aux autres utilisateurs (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="1abd9-126">Denies write permission to other users (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1abd9-127"><strong>dbInconsistent</strong></span><span class="sxs-lookup"><span data-stu-id="1abd9-127"><strong>dbInconsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="1abd9-128">(Option par défaut) Exécute les mises à jour incohérentes (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="1abd9-128">(Default) Executes inconsistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1abd9-129"><strong>dbConsistent</strong></span><span class="sxs-lookup"><span data-stu-id="1abd9-129"><strong>dbConsistent</strong></span></span></p></td>
<td><p><span data-ttu-id="1abd9-130">Exécute les mises à jour cohérentes (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="1abd9-130">Executes consistent updates (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1abd9-131"><strong>dbSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="1abd9-131"><strong>dbSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="1abd9-p101">Exécute une requête SQL directe. Si elle est définie, cette option transmet l'instruction SQL à une base de données ODBC pour traitement (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="1abd9-p101">Executes an SQL pass-through query. Setting this option passes the SQL statement to an ODBC database for processing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1abd9-134"><strong>dbFailOnError</strong></span><span class="sxs-lookup"><span data-stu-id="1abd9-134"><strong>dbFailOnError</strong></span></span></p></td>
<td><p><span data-ttu-id="1abd9-135">Annule les mises à jour si une erreur se produit (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="1abd9-135">Rolls back updates if an error occurs (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1abd9-136"><strong>dbSeeChanges</strong></span><span class="sxs-lookup"><span data-stu-id="1abd9-136"><strong>dbSeeChanges</strong></span></span></p></td>
<td><p><span data-ttu-id="1abd9-137">Génère une erreur d'exécution si un autre utilisateur modifie les données que vous-même êtes en train de modifier (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="1abd9-137">Generates a run-time error if another user is changing data you are editing (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1abd9-138"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="1abd9-138"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="1abd9-139">Exécute la requête en mode asynchrone (objets ODBCDirect Connection et QueryDef uniquement).</span><span class="sxs-lookup"><span data-stu-id="1abd9-139">Executes the query asynchronously (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1abd9-140"><strong>dbExecDirect</strong></span><span class="sxs-lookup"><span data-stu-id="1abd9-140"><strong>dbExecDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="1abd9-141">Exécute l'instruction sans appeler préalablement la fonction API ODBC SQLPrepare (objets ODBCDirect Connection et QueryDef uniquement).</span><span class="sxs-lookup"><span data-stu-id="1abd9-141">Executes the statement without first calling SQLPrepare ODBC API function (ODBCDirect Connection and QueryDef objects only).</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1abd9-p102">Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="1abd9-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

> [!NOTE]
> <span data-ttu-id="1abd9-p103">Les constantes **dbConsistent** et **dbInconsistent** s’excluent mutuellement. Vous pouvez utiliser l’une ou l’autre dans une instance donnée d’**OpenRecordset**, mais pas les deux à la fois. L’utilisation simultanée de **dbConsistent** et **dbInconsistent** entraîne une erreur.</span><span class="sxs-lookup"><span data-stu-id="1abd9-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive. You can use one or the other, but not both in a given instance of **OpenRecordset**. Using both **dbConsistent** and **dbInconsistent** causes an error.</span></span>

<span data-ttu-id="1abd9-p104">La méthode **Execute** est valide uniquement pour les requêtes Action. Si vous utilisez **Execute** avec un autre type de requête, une erreur est générée. Dans la mesure où une requête Action ne renvoie aucun enregistrement, **Execute** ne renvoie pas d'objet **Recordset** (l'exécution d'une requête SQL directe dans un espace de travail ODBCDirect ne renvoie pas d'erreur si aucun objet **Recordset** n'est renvoyé).</span><span class="sxs-lookup"><span data-stu-id="1abd9-p104">The **Execute** method is valid only for action queries. If you use **Execute** with another type of query, an error occurs. Because an action query doesn't return any records, **Execute** doesn't return a **Recordset**. (Executing an SQL pass-through query in an ODBCDirect workspace will not return an error if a **Recordset** isn't returned.)</span></span>

<span data-ttu-id="1abd9-p105">Utilisez la propriété **RecordsAffected** de l'objet **Connection**, **Database** ou **QueryDef** pour déterminer le nombre d'enregistrements affectés par le dernier appel de la méthode **Execute**. **RecordsAffected** contient, par exemple, le nombre d'enregistrements supprimés, mis à jour ou insérés lors de l'exécution d'une requête Action. Lorsque vous utilisez la méthode **Execute** pour exécuter une requête, la propriété **RecordsAffected** de l'objet **QueryDef** a pour valeur le nombre d'enregistrements affectés.</span><span class="sxs-lookup"><span data-stu-id="1abd9-p105">Use the **RecordsAffected** property of the **Connection**, **Database**, or **QueryDef** object to determine the number of records affected by the most recent **Execute** method. For example, **RecordsAffected** contains the number of records deleted, updated, or inserted when executing an action query. When you use the **Execute** method to run a query, the **RecordsAffected** property of the **QueryDef** object is set to the number of records affected.</span></span>

<span data-ttu-id="1abd9-p106">Dans un espace de travail Microsoft Access, si vous fournissez une instruction SQL correcte du point de vue syntaxique et que vous détenez les autorisations appropriées, la méthode **Execute** n’échouera pas, même si aucune ligne ne peut être modifiée ou supprimée. Par conséquent, utilisez toujours l’option **dbFailOnError** lorsque vous vous servez de la méthode **Execute** pour exécuter une requête Mise à jour ou Suppression. Cette option génère une erreur d’exécution et annule toutes les modifications accomplies dans le cas où certains enregistrements affectés sont verrouillés et ne peuvent pas être mis à jour ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="1abd9-p106">In a Microsoft Access workspace, if you provide a syntactically correct SQL statement and have the appropriate permissions, the **Execute** method won't fail — even if not a single row can be modified or deleted. Therefore, always use the **dbFailOnError** option when using the **Execute** method to run an update or delete query. This option generates a run-time error and rolls back all successful changes if any of the records affected are locked and can't be updated or deleted.</span></span>

<span data-ttu-id="1abd9-p107">Dans les versions antérieures du moteur de base de données Microsoft Jet, les instructions SQL étaient automatiquement incorporées dans des transactions implicites. Si une partie d’une instruction exécutée avec **dbFailOnError** échouait, l’instruction était entièrement annulée. Dans un souci d’amélioration des performances, ces transactions implicites ont été supprimées à compter de la version 3.5. Si vous mettez à jour un code DAO plus ancien, envisagez l’utilisation de transactions explicites autour des instructions **Execute**.</span><span class="sxs-lookup"><span data-stu-id="1abd9-p107">In earlier versions of the Microsoft Jet database engine, SQL statements were automatically embedded in implicit transactions. If part of a statement executed with **dbFailOnError** failed, the entire statement would be rolled back. To improve performance, these implicit transactions were removed starting with version 3.5. If you are updating older DAO code, be sure to consider using explicit transactions around **Execute** statements.</span></span>

<span data-ttu-id="1abd9-p108">Pour obtenir de meilleures performances dans un espace de travail Microsoft Access, en particulier dans un environnement multi-utilisateur, imbriquez la méthode **Execute** dans une transaction. Utilisez la méthode **BeginTrans** sur l'objet **Workspace** actif, puis utilisez la méthode **Execute** et terminez la transaction en appelant la méthode **CommitTrans** sur l'objet **Workspace**. Cette opération permet d'enregistrer les modifications sur disque et de libérer tous les verrous appliqués pendant l'exécution de la requête.</span><span class="sxs-lookup"><span data-stu-id="1abd9-p108">For best performance in a Microsoft Access workspace, especially in a multiuser environment, nest the **Execute** method inside a transaction. Use the **BeginTrans** method on the current **Workspace** object, then use the **Execute** method, and complete the transaction by using the **CommitTrans** method on the **Workspace**. This saves changes on disk and frees any locks placed while the query is running.</span></span>

