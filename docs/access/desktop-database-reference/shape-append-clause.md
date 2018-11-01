---
title: APPEND, clause de commande SHAPE
TOCTitle: Shape Append Clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca7d84e0a0fe1eda9237a4743a3296de7f192053
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879115"
---
# <a name="shape-append-clause"></a><span data-ttu-id="10300-102">Shape Append, clause</span><span class="sxs-lookup"><span data-stu-id="10300-102">Shape Append Clause</span></span>


<span data-ttu-id="10300-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10300-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10300-p101">La clause APPEND de commande SHAPE ajoute une ou plusieurs colonnes à un objet **Recordset**. Souvent, ces colonnes sont des chapitres qui font référence à un objet **Recordset** enfant.</span><span class="sxs-lookup"><span data-stu-id="10300-p101">The shape command APPEND clause appends a column or columns to a **Recordset**. Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="10300-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10300-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="10300-107">Description</span><span class="sxs-lookup"><span data-stu-id="10300-107">Description</span></span>

<span data-ttu-id="10300-108">Cette clause comporte les parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="10300-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="10300-109">*parent-command*</span><span class="sxs-lookup"><span data-stu-id="10300-109">*parent-command*</span></span>

- <span data-ttu-id="10300-110">Zéro ou un des éléments suivants (vous pouvez omettre la *parent-command* complètement) :</span><span class="sxs-lookup"><span data-stu-id="10300-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="10300-p102">Commande fournisseur entre accolades (« {} ») qui retourne un objet **Recordset**. La commande est transmise au fournisseur de données sous-jacent et sa syntaxe dépend des exigences du fournisseur. Elle est en général écrite en langage SQL, même si ADO n'exige pas de langage de requête particulier.</span><span class="sxs-lookup"><span data-stu-id="10300-p102">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="10300-114">Autre commande Shape placée entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="10300-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="10300-115">Mot-clé TABLE, suivi du nom d'une table du fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="10300-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="10300-116">*parent-alias*</span><span class="sxs-lookup"><span data-stu-id="10300-116">*parent-alias*</span></span>

  - <span data-ttu-id="10300-117">Alias facultatif qui fait référence à l'objet **Recordset** parent.</span><span class="sxs-lookup"><span data-stu-id="10300-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="10300-118">*column-list*</span><span class="sxs-lookup"><span data-stu-id="10300-118">*column-list*</span></span>

  - <span data-ttu-id="10300-119">Un ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="10300-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="10300-120">Colonne agrégée.</span><span class="sxs-lookup"><span data-stu-id="10300-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="10300-121">Colonne calculée.</span><span class="sxs-lookup"><span data-stu-id="10300-121">A calculated column.</span></span>
    
    - <span data-ttu-id="10300-122">Nouvelle colonne créée avec la clause NEW.</span><span class="sxs-lookup"><span data-stu-id="10300-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="10300-p103">Colonne de chapitre. Une définition de colonne de chapitre est placée entre parenthèses (« () »). Reportez-vous à la syntaxe ci-dessous</span><span class="sxs-lookup"><span data-stu-id="10300-p103">A chapter column. A chapter column definition is enclosed in parentheses ("()"). See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="10300-126">*child-recordset*</span><span class="sxs-lookup"><span data-stu-id="10300-126">*child-recordset*</span></span>

  - <span data-ttu-id="10300-p104">Commande fournisseur entre accolades (« {} ») qui retourne un objet **Recordset**. La commande est transmise au fournisseur de données sous-jacent et sa syntaxe dépend des exigences du fournisseur. Elle est en général écrite en langage SQL, même si ADO n'exige pas de langage de requête particulier.</span><span class="sxs-lookup"><span data-stu-id="10300-p104">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="10300-130">Autre commande Shape placée entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="10300-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="10300-131">Nom d'un objet **Recordset** mis en forme existant.</span><span class="sxs-lookup"><span data-stu-id="10300-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="10300-132">Mot-clé TABLE, suivi du nom d'une table du fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="10300-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="10300-133">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="10300-133">*child-alias*</span></span>

  - <span data-ttu-id="10300-134">Alias qui fait référence à l'objet **Recordset** enfant.</span><span class="sxs-lookup"><span data-stu-id="10300-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="10300-135">*parent-column*</span><span class="sxs-lookup"><span data-stu-id="10300-135">*parent-column*</span></span>

  - <span data-ttu-id="10300-136">Une colonne dans le **jeu d’enregistrements** renvoyé par la *parent-command.*</span><span class="sxs-lookup"><span data-stu-id="10300-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="10300-137">*child-column*</span><span class="sxs-lookup"><span data-stu-id="10300-137">*child-column*</span></span>

  - <span data-ttu-id="10300-138">Colonne de l'objet **Recordset** retournée par *child-command*.</span><span class="sxs-lookup"><span data-stu-id="10300-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="10300-139">*param-number*</span><span class="sxs-lookup"><span data-stu-id="10300-139">*param-number*</span></span>

  - <span data-ttu-id="10300-140">Consultez [Fonctionnement des commandes paramétrées](operation-of-parameterized-commands.md).</span><span class="sxs-lookup"><span data-stu-id="10300-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="10300-141">*chapter-alias*</span><span class="sxs-lookup"><span data-stu-id="10300-141">*chapter-alias*</span></span>

  - <span data-ttu-id="10300-142">Alias qui fait référence à la colonne de chapitre ajoutée au parent.</span><span class="sxs-lookup"><span data-stu-id="10300-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="10300-143">La clause _« parent-column à colonne-enfant »_ est en fait une liste, dans laquelle chaque relation définie est séparée par une virgule.</span><span class="sxs-lookup"><span data-stu-id="10300-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="10300-144">[!REMARQUE] La clause suivant le mot-clé APPEND est en fait une liste, dans laquelle chaque clause est séparée par une virgule et définit une autre colonne à ajouter au parent.</span><span class="sxs-lookup"><span data-stu-id="10300-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="10300-145">Notes</span><span class="sxs-lookup"><span data-stu-id="10300-145">Remarks</span></span>

<span data-ttu-id="10300-p105">Lorsque vous créez des commandes de fournisseur depuis une entrée utilisateur dans le cadre d'une commande SHAPE, SHAPE traite la commande fournisseur fournie par l'utilisateur sous la forme d'une chaîne opaque et la passe fidèlement au fournisseur. Par exemple, dans la commande SHAPE suivante,</span><span class="sxs-lookup"><span data-stu-id="10300-p105">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider. For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="10300-148">SHAPE exécute deux commandes : sélectionnez \* de t1 et (sélectionnez \* from t2 associer k1 TO k2).</span><span class="sxs-lookup"><span data-stu-id="10300-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="10300-149">Si l'utilisateur fournit une commande composée de plusieurs commandes fournisseur séparées par des points-virgules, SHAPE ne sera pas capable de discerner les composantes de la commande.</span><span class="sxs-lookup"><span data-stu-id="10300-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="10300-150">Ainsi, dans la commande SHAPE suivante,</span><span class="sxs-lookup"><span data-stu-id="10300-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="10300-151">FORME exécute sélectionner \* de t1 ; DROP table t1 et (sélectionnez \* from t2 associer k1 TO k2), sans réaliser que drop table t1 est distincte et dans cette commande fournisseur cas, dangereuse.</span><span class="sxs-lookup"><span data-stu-id="10300-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="10300-152">Les applications doivent toujours valider l'entrée utilisateur pour empêcher d'éventuelles attaques de pirates.</span><span class="sxs-lookup"><span data-stu-id="10300-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>

<span data-ttu-id="10300-153">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="10300-153">This section includes the following topics:</span></span>

- [<span data-ttu-id="10300-154">Fonctionnement des commandes non paramétrées</span><span class="sxs-lookup"><span data-stu-id="10300-154">Operation of Non-Parameterized Commands</span></span>](operation-of-non-parameterized-commands.md)

- [<span data-ttu-id="10300-155">Fonctionnement des commandes paramétrées</span><span class="sxs-lookup"><span data-stu-id="10300-155">Operation of Parameterized Commands</span></span>](operation-of-parameterized-commands.md)

- [<span data-ttu-id="10300-156">Commandes hybrides</span><span class="sxs-lookup"><span data-stu-id="10300-156">Hybrid Commands</span></span>](hybrid-commands.md)

- [<span data-ttu-id="10300-157">Clauses de mise en forme COMPUTE intermédiaires</span><span class="sxs-lookup"><span data-stu-id="10300-157">Intervening Shape COMPUTE Clauses</span></span>](intervening-shape-compute-clauses.md)