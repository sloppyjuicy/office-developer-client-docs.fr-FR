---
title: Bloc de données RechercherEnregistrement
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7a5cccb77300f36f3e33cd1eccb6c6d278db3120
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734209"
---
# <a name="lookuprecord-data-block"></a><span data-ttu-id="46705-102">Bloc de données RechercherEnregistrement</span><span class="sxs-lookup"><span data-stu-id="46705-102">LookupRecord data block</span></span>

<span data-ttu-id="46705-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46705-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46705-104">Un bloc de données **RechercherEnregistrement** effectue un ensemble d'actions sur un enregistrement spécifique.</span><span class="sxs-lookup"><span data-stu-id="46705-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="46705-105">Le bloc de données **RechercherEnregistrement** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="46705-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="46705-106">Setting</span><span class="sxs-lookup"><span data-stu-id="46705-106">Setting</span></span>

<span data-ttu-id="46705-107">L’action **DéfinirChamp** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="46705-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46705-108">Argument</span><span class="sxs-lookup"><span data-stu-id="46705-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="46705-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="46705-109">Required</span></span></p></th>
<th><p><span data-ttu-id="46705-110">Description</span><span class="sxs-lookup"><span data-stu-id="46705-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46705-111">Dans le paramètre</span><span class="sxs-lookup"><span data-stu-id="46705-111">In</span></span></p></td>
<td><p><span data-ttu-id="46705-112">Oui</span><span class="sxs-lookup"><span data-stu-id="46705-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="46705-113">Chaîne qui identifie l’enregistrement sur lequel opérer.</span><span class="sxs-lookup"><span data-stu-id="46705-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="46705-114">L’argument <em>dans</em> peut contenir le nom de la table, une requête sélection ou une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="46705-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="46705-115"><strong>Remarque</strong>: l’enregistrement spécifié ne peut pas inclure de données stockées dans une table liée ou une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="46705-115"><strong>NOTE</strong>: The specified record cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46705-116">Condition Where</span><span class="sxs-lookup"><span data-stu-id="46705-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="46705-117">Non</span><span class="sxs-lookup"><span data-stu-id="46705-117">No</span></span></p></td>
<td><p><span data-ttu-id="46705-118">Expression de type Chaîne qui permet de restreindre la plage de données sur laquelle opère le bloc de données <strong>RechercherEnregistrement</strong>.</span><span class="sxs-lookup"><span data-stu-id="46705-118">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed.</span></span> <span data-ttu-id="46705-119">Par exemple, les critères sont souvent équivalents à la clause WHERE d’une expression SQL, sans le mot WHERE.</span><span class="sxs-lookup"><span data-stu-id="46705-119">For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="46705-120">Si les critères sont omis, le bloc de données <strong>RechercherEnregistrement</strong> opère sur tout le domaine spécifié par l’argument <em>dans</em> .</span><span class="sxs-lookup"><span data-stu-id="46705-120">If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="46705-121">Tout champ inclus dans les critères doit également être un champ dans <em>In</em>.</span><span class="sxs-lookup"><span data-stu-id="46705-121">Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46705-122">Alias</span><span class="sxs-lookup"><span data-stu-id="46705-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="46705-123">Non</span><span class="sxs-lookup"><span data-stu-id="46705-123">No</span></span></p></td>
<td><p><span data-ttu-id="46705-124">Chaîne qui fournit un autre nom pour l’enregistrement spécifié par l’argument <em>dans</em> .</span><span class="sxs-lookup"><span data-stu-id="46705-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="46705-125">On l’utilise souvent pour raccourcir le nom de la table pour les références ultérieures, afin d’éviter d’éventuelles références ambiguës.</span><span class="sxs-lookup"><span data-stu-id="46705-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="46705-126">Si <em>Alias</em> n’est pas spécifié, le nom de la table ou de la requête est utilisé comme alias.</span><span class="sxs-lookup"><span data-stu-id="46705-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="46705-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="46705-127">Remarks</span></span>

<span data-ttu-id="46705-128">Si les critères spécifiés par les arguments dans la condition dans et *Where* renvoient plus d’un enregistrement, le bloc *de* données **RechercherEnregistrement** fonctionne uniquement sur le premier enregistrement.</span><span class="sxs-lookup"><span data-stu-id="46705-128">If the criteria specified by the *In* and *Where Condition* arguments returns more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>  <span data-ttu-id="46705-129">Si aucun enregistrement ne correspond aux critères spécifiés, Access ignore l’ensemble d’actions contenues dans le bloc **RechercherEnregistrement** , comme s’il avait **[été une expression](if-then-else-macro-block.md)** de bloc de macros évaluée comme false.</span><span class="sxs-lookup"><span data-stu-id="46705-129">In the case that no records match the specified criteria, Access will skip over the set of actions contained within the **LookupRecord** block, as if it had been an **[If](if-then-else-macro-block.md)** macro block expression that evaluated as false.</span></span>

## <a name="example"></a><span data-ttu-id="46705-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="46705-130">Example</span></span>

<span data-ttu-id="46705-131">L’exemple suivant montre comment utiliser l’action SetReturnVar pour renvoyer une valeur à partir d’une macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="46705-131">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="46705-132">Une ReturnVar nommée **CurrentServiceRequest** est renvoyée à la macro ou à la sous-routine Visual Basic pour applications (VBA) qui a appelé la macro de données nommée.</span><span class="sxs-lookup"><span data-stu-id="46705-132">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="46705-133">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="46705-133">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="46705-134">L’exemple suivant montre comment utiliser l’action Déclenchererreur pour annuler l’événement de macro avant la modification des données.</span><span class="sxs-lookup"><span data-stu-id="46705-134">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="46705-135">Lorsque le champ AffectéÀ est mis à jour, un bloc de données RechercherEnregistrement est utilisé pour déterminer si le technicien affecté est actuellement affecté à une demande de service ouverte.</span><span class="sxs-lookup"><span data-stu-id="46705-135">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="46705-136">Si la valeur est true, l’événement avant la modification est annulé et l’enregistrement n’est pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="46705-136">If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

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
