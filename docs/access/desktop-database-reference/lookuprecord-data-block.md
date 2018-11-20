---
title: Bloc de données RechercherEnregistrement
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c93f312dd9b43a3235f049b9e6d3f95d08eba87f
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025594"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="307ca-102">Bloc de données RechercherEnregistrement</span><span class="sxs-lookup"><span data-stu-id="307ca-102">LookupRecord data block</span></span>

<span data-ttu-id="307ca-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="307ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="307ca-104">Un bloc de données **RechercherEnregistrement** effectue un ensemble d'actions sur un enregistrement spécifique.</span><span class="sxs-lookup"><span data-stu-id="307ca-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="307ca-105">[!REMARQUE] Le bloc de données **RechercherEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="307ca-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="307ca-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="307ca-106">Setting</span></span>

<span data-ttu-id="307ca-107">L'action **DéfinirChamp** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="307ca-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="307ca-108">Argument</span><span class="sxs-lookup"><span data-stu-id="307ca-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="307ca-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="307ca-109">Required</span></span></p></th>
<th><p><span data-ttu-id="307ca-110">Description</span><span class="sxs-lookup"><span data-stu-id="307ca-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="307ca-111">Dans le paramètre</span><span class="sxs-lookup"><span data-stu-id="307ca-111">In</span></span></p></td>
<td><p><span data-ttu-id="307ca-112">Oui</span><span class="sxs-lookup"><span data-stu-id="307ca-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="307ca-113">Une chaîne qui identifie l’enregistrement à utiliser.</span><span class="sxs-lookup"><span data-stu-id="307ca-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="307ca-114">L’argument <em>dans</em> peut contenir le nom de la table, une requête sélection ou une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="307ca-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="307ca-115"><strong>Remarque</strong>: l’enregistrement spécifié ne peut pas inclure les données stockées dans une table liée ou d’une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="307ca-115"><strong>NOTE</strong>: The specified record cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="307ca-116">Condition Where</span><span class="sxs-lookup"><span data-stu-id="307ca-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="307ca-117">Non</span><span class="sxs-lookup"><span data-stu-id="307ca-117">No</span></span></p></td>
<td><p><span data-ttu-id="307ca-118">Une expression de chaîne utilisée pour limiter la plage de données sur lequel le bloc de données <strong>RechercherEnregistrement</strong> est effectuée.</span><span class="sxs-lookup"><span data-stu-id="307ca-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="307ca-119">Par exemple, les critères sont souvent équivalents à la clause WHERE d’une expression SQL sans le mot où.</span><span class="sxs-lookup"><span data-stu-id="307ca-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="307ca-120">Si les critères sont tous deux omis, le bloc de données <strong>RechercherEnregistrement</strong> opère sur l’intégralité du domaine spécifié par l’argument <em>dans</em> .</span><span class="sxs-lookup"><span data-stu-id="307ca-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="307ca-121">Un champ qui est inclus dans les critères doit également être un champ <em>dans</em>.</span><span class="sxs-lookup"><span data-stu-id="307ca-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="307ca-122">Alias</span><span class="sxs-lookup"><span data-stu-id="307ca-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="307ca-123">Non</span><span class="sxs-lookup"><span data-stu-id="307ca-123">No</span></span></p></td>
<td><p><span data-ttu-id="307ca-124">Chaîne qui fournit un autre nom pour l’enregistrement spécifié par l’argument <em>dans</em> .</span><span class="sxs-lookup"><span data-stu-id="307ca-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="307ca-125">Souvent utilisés pour raccourcir le nom de table de références ultérieures éviter d’éventuelles références ambigus.</span><span class="sxs-lookup"><span data-stu-id="307ca-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="307ca-126">Si <em>Alias</em> n’est pas spécifié, le nom de la table ou de la requête est utilisé comme alias.</span><span class="sxs-lookup"><span data-stu-id="307ca-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="307ca-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="307ca-127">Remarks</span></span>

<span data-ttu-id="307ca-128">Si les critères spécifiés par les arguments *dans* et *Condition Where* spécifie plusieurs enregistrements, le bloc de données **RechercherEnregistrement** fonctionne uniquement sur le premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="307ca-128">If the criteria specified by the *In* and *Where Condition* arguments specifies more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>

## <a name="example"></a><span data-ttu-id="307ca-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="307ca-129">Example</span></span>

<span data-ttu-id="307ca-130">L’exemple suivant montre comment utiliser l’action SetReturnVar pour renvoyer une valeur d’une macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="307ca-130">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="307ca-131">Un ReturnVar nommé **CurrentServiceRequest** est renvoyé à la macro ou de Visual Basic pour sous-routine Applications (VBA) qui a appelé la macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="307ca-131">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="307ca-132">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="307ca-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```

<br/>

<span data-ttu-id="307ca-133">L’exemple suivant montre comment utiliser l’action Déclenchererreur pour annuler l’événement de macro de données avant la modification.</span><span class="sxs-lookup"><span data-stu-id="307ca-133">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="307ca-134">Lorsque le champ AssignedTo est mis à jour, un bloc de données RechercherEnregistrement permet de déterminer si le technicien affecté est actuellement affecté à une demande de service en cours.</span><span class="sxs-lookup"><span data-stu-id="307ca-134">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="307ca-135">Si la valeur est true, l’événement avant la modification est annulée et l’enregistrement n’est pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="307ca-135">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
