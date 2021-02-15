---
title: RaiseError, action de macro
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b706ffed14fdb440f3c3192c7c36015343f2e134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300923"
---
# <a name="raiseerror-macro-action"></a><span data-ttu-id="4fcc9-102">RaiseError, action de macro</span><span class="sxs-lookup"><span data-stu-id="4fcc9-102">RaiseError macro action</span></span>

<span data-ttu-id="4fcc9-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4fcc9-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="4fcc9-104">L'action **DéclencherErreur** lève une exception qui peut être gérée par l'action de macro **[SurErreur](onerror-macro-action.md)**.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-104">The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.</span></span>

> [!NOTE]
> <span data-ttu-id="4fcc9-105">[!REMARQUE] L'action **DéclencherErreur** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-105">The **RaiseError** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="4fcc9-106">Setting</span><span class="sxs-lookup"><span data-stu-id="4fcc9-106">Setting</span></span>

<span data-ttu-id="4fcc9-107">L’action **DéclencherErreur** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-107">The **RaiseError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4fcc9-108">Argument</span><span class="sxs-lookup"><span data-stu-id="4fcc9-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="4fcc9-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4fcc9-109">Required</span></span></p></th>
<th><p><span data-ttu-id="4fcc9-110">Description</span><span class="sxs-lookup"><span data-stu-id="4fcc9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4fcc9-111">Numéro d’erreur</span><span class="sxs-lookup"><span data-stu-id="4fcc9-111">Error Number</span></span></p></td>
<td><p><span data-ttu-id="4fcc9-112">Oui</span><span class="sxs-lookup"><span data-stu-id="4fcc9-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="4fcc9-113">Nombre ou expression résolu au type de données Long.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-113">A number or an expression that resolves to the Long data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fcc9-114">Description de l’erreur</span><span class="sxs-lookup"><span data-stu-id="4fcc9-114">Error Description</span></span></p></td>
<td><p><span data-ttu-id="4fcc9-115">Non</span><span class="sxs-lookup"><span data-stu-id="4fcc9-115">No</span></span></p></td>
<td><p><span data-ttu-id="4fcc9-116">Expression de type Chaîne qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-116">A string expression that describes the error.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4fcc9-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="4fcc9-117">Remarks</span></span>

<span data-ttu-id="4fcc9-118">Si l'action **DéclencherErreur** est appelée dans un événement de macro **[Avant la modification](before-change-macro-event.md)** ou **[Avant la suppression](before-delete-macro-event.md)**, l'événement est annulé.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-118">If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.</span></span>

<span data-ttu-id="4fcc9-p101">S'il n'y a aucune instruction **SurErreur** active qui gère les erreurs, l'erreur levée par l'action **DéclencherErreur** est ajoutée à la table système **USysApplicationLog**. Lorsque l'action **DéclencherErreur** écrit dans la table **USysApplicationLog**, la colonne **Catégorie** prend automatiquement la valeur **Exécution**.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-p101">If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table. When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.</span></span>

<span data-ttu-id="4fcc9-121">Pour afficher la table **USysApplicationLog**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="4fcc9-121">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="4fcc9-122">Cliquez sur **le** menu Fichier, puis sur **Options.**</span><span class="sxs-lookup"><span data-stu-id="4fcc9-122">Click the **File** menu, and then click **Options**.</span></span>

2.  <span data-ttu-id="4fcc9-123">Dans la boîte dialogue **Options Access**, cliquez sur l'onglet **Base de données active**.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-123">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="4fcc9-124">Dans la section **Navigation**, cliquez sur **Options de navigation**.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-124">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="4fcc9-125">Dans la boîte de dialogue **Options de navigation**, cliquez sur **Afficher les objets système**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-125">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="4fcc9-126">Cliquez sur **OK** pour fermer la boîte de dialogue **Options Access**.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-126">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="4fcc9-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="4fcc9-127">Example</span></span>

<span data-ttu-id="4fcc9-128">L’exemple suivant montre comment utiliser l’action RaiseError pour annuler l’événement de macro de données Avant la modification.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-128">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="4fcc9-129">Lorsque le champ AssignedTo est mis à jour, un bloc de données LookupRecord est utilisé pour déterminer si le technicien affecté est actuellement affecté à une demande de service ouverte.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-129">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="4fcc9-130">Si c’est le cas, l’événement Before Change est annulé et l’enregistrement n’est pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4fcc9-130">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="4fcc9-131">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4fcc9-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
