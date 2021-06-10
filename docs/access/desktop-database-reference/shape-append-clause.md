---
title: Shape Append, clause
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40c35e8b2c3fb3f0b92bf261b62c252a61a367b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306446"
---
# <a name="shape-append-clause"></a><span data-ttu-id="37a12-102">Shape Append, clause</span><span class="sxs-lookup"><span data-stu-id="37a12-102">Shape Append clause</span></span>


<span data-ttu-id="37a12-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="37a12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37a12-p101">La clause APPEND de commande SHAPE ajoute une ou plusieurs colonnes à un objet **Recordset**. Souvent, ces colonnes sont des chapitres qui font référence à un objet **Recordset** enfant.</span><span class="sxs-lookup"><span data-stu-id="37a12-p101">The shape command APPEND clause appends a column or columns to a **Recordset**. Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a12-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37a12-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="37a12-107">Description</span><span class="sxs-lookup"><span data-stu-id="37a12-107">Description</span></span>

<span data-ttu-id="37a12-108">Cette clause comporte les parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="37a12-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="37a12-109">*parent-command*</span><span class="sxs-lookup"><span data-stu-id="37a12-109">*parent-command*</span></span>

- <span data-ttu-id="37a12-110">Un des éléments suivants ou aucun (vous pouvez omettre *parent-command* complètement) :</span><span class="sxs-lookup"><span data-stu-id="37a12-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="37a12-p102">Commande fournisseur entre accolades (« {} ») qui retourne un objet **Recordset**. La commande est transmise au fournisseur de données sous-jacent et sa syntaxe dépend des exigences du fournisseur. Elle est en général écrite en langage SQL, même si ADO n'exige pas de langage de requête particulier.</span><span class="sxs-lookup"><span data-stu-id="37a12-p102">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="37a12-114">Autre commande Shape placée entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="37a12-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="37a12-115">Mot-clé TABLE, suivi du nom d'une table du fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="37a12-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="37a12-116">*parent-alias*</span><span class="sxs-lookup"><span data-stu-id="37a12-116">*parent-alias*</span></span>

  - <span data-ttu-id="37a12-117">Alias facultatif qui fait référence à l'objet **Recordset** parent.</span><span class="sxs-lookup"><span data-stu-id="37a12-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="37a12-118">*column-list*</span><span class="sxs-lookup"><span data-stu-id="37a12-118">*column-list*</span></span>

  - <span data-ttu-id="37a12-119">Un ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="37a12-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="37a12-120">Colonne agrégée.</span><span class="sxs-lookup"><span data-stu-id="37a12-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="37a12-121">Colonne calculée.</span><span class="sxs-lookup"><span data-stu-id="37a12-121">A calculated column.</span></span>
    
    - <span data-ttu-id="37a12-122">Nouvelle colonne créée avec la clause NEW.</span><span class="sxs-lookup"><span data-stu-id="37a12-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="37a12-p103">Colonne de chapitre. Une définition de colonne de chapitre est placée entre parenthèses (« () »). Reportez-vous à la syntaxe ci-dessous</span><span class="sxs-lookup"><span data-stu-id="37a12-p103">A chapter column. A chapter column definition is enclosed in parentheses ("()"). See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="37a12-126">*child-recordset*</span><span class="sxs-lookup"><span data-stu-id="37a12-126">*child-recordset*</span></span>

  - <span data-ttu-id="37a12-p104">Commande fournisseur entre accolades (« {} ») qui retourne un objet **Recordset**. La commande est transmise au fournisseur de données sous-jacent et sa syntaxe dépend des exigences du fournisseur. Elle est en général écrite en langage SQL, même si ADO n'exige pas de langage de requête particulier.</span><span class="sxs-lookup"><span data-stu-id="37a12-p104">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="37a12-130">Autre commande Shape placée entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="37a12-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="37a12-131">Nom d'un objet **Recordset** mis en forme existant.</span><span class="sxs-lookup"><span data-stu-id="37a12-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="37a12-132">Mot-clé TABLE, suivi du nom d'une table du fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="37a12-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="37a12-133">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="37a12-133">*child-alias*</span></span>

  - <span data-ttu-id="37a12-134">Alias qui fait référence à l'objet **Recordset** enfant.</span><span class="sxs-lookup"><span data-stu-id="37a12-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="37a12-135">*parent-column*</span><span class="sxs-lookup"><span data-stu-id="37a12-135">*parent-column*</span></span>

  - <span data-ttu-id="37a12-136">Colonne de l'objet **Recordset** retournée par *parent-command.*</span><span class="sxs-lookup"><span data-stu-id="37a12-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="37a12-137">*child-column*</span><span class="sxs-lookup"><span data-stu-id="37a12-137">*child-column*</span></span>

  - <span data-ttu-id="37a12-138">Colonne de l'objet **Recordset** retournée par *child-command*.</span><span class="sxs-lookup"><span data-stu-id="37a12-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="37a12-139">*param-number*</span><span class="sxs-lookup"><span data-stu-id="37a12-139">*param-number*</span></span>

  - <span data-ttu-id="37a12-140">Consultez [Fonctionnement des commandes paramétrées](operation-of-parameterized-commands.md).</span><span class="sxs-lookup"><span data-stu-id="37a12-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="37a12-141">*chapter-alias*</span><span class="sxs-lookup"><span data-stu-id="37a12-141">*chapter-alias*</span></span>

  - <span data-ttu-id="37a12-142">Alias qui fait référence à la colonne de chapitre ajoutée au parent.</span><span class="sxs-lookup"><span data-stu-id="37a12-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="37a12-143">La clause _« parent-column TO child-column »_ est en fait une liste, où chaque relation définie est séparée par une virgule.</span><span class="sxs-lookup"><span data-stu-id="37a12-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="37a12-144">La clause suivant le mot-clé APPEND est en fait une liste, dans laquelle chaque clause est séparée par une virgule et définit une autre colonne à ajouter au parent.</span><span class="sxs-lookup"><span data-stu-id="37a12-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="37a12-145">Remarques</span><span class="sxs-lookup"><span data-stu-id="37a12-145">Remarks</span></span>

<span data-ttu-id="37a12-p105">Lorsque vous créez des commandes de fournisseur depuis une entrée utilisateur dans le cadre d'une commande SHAPE, SHAPE traite la commande fournisseur fournie par l'utilisateur sous la forme d'une chaîne opaque et la passe fidèlement au fournisseur. Par exemple, dans la commande SHAPE suivante,</span><span class="sxs-lookup"><span data-stu-id="37a12-p105">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider. For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="37a12-148">SHAPE exécute deux commandes : select \* from t1 et (select \* from t2 RELATE k1 TO k2).</span><span class="sxs-lookup"><span data-stu-id="37a12-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="37a12-149">Si l'utilisateur fournit une commande composée de plusieurs commandes fournisseur séparées par des points-virgules, SHAPE ne sera pas capable de discerner les composantes de la commande.</span><span class="sxs-lookup"><span data-stu-id="37a12-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="37a12-150">Ainsi, dans la commande SHAPE suivante,</span><span class="sxs-lookup"><span data-stu-id="37a12-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="37a12-151">SHAPE exécute select \* from t1; drop table t1 et (select from t2 RELATE k1 TO k2), sans se rendre compte que le tableau de drop t1 est une commande de fournisseur distincte et, dans ce \* cas, dangereuse.</span><span class="sxs-lookup"><span data-stu-id="37a12-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="37a12-152">Les applications doivent toujours valider l'entrée utilisateur pour empêcher d'éventuelles attaques de pirates.</span><span class="sxs-lookup"><span data-stu-id="37a12-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>

<span data-ttu-id="37a12-153">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="37a12-153">This section includes the following topics:</span></span>

- [<span data-ttu-id="37a12-154">Operation of Non-Parameterized Commands</span><span class="sxs-lookup"><span data-stu-id="37a12-154">Operation of Non-Parameterized Commands</span></span>](operation-of-non-parameterized-commands.md)

- [<span data-ttu-id="37a12-155">Operation of Parameterized Commands</span><span class="sxs-lookup"><span data-stu-id="37a12-155">Operation of Parameterized Commands</span></span>](operation-of-parameterized-commands.md)

- [<span data-ttu-id="37a12-156">Hybrid Commands</span><span class="sxs-lookup"><span data-stu-id="37a12-156">Hybrid Commands</span></span>](hybrid-commands.md)

- [<span data-ttu-id="37a12-157">Intervening Shape COMPUTE Clauses</span><span class="sxs-lookup"><span data-stu-id="37a12-157">Intervening Shape COMPUTE Clauses</span></span>](intervening-shape-compute-clauses.md)
