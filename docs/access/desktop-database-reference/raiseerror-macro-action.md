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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726035"
---
# <a name="raiseerror-macro-action"></a><span data-ttu-id="dff03-102">RaiseError, action de macro</span><span class="sxs-lookup"><span data-stu-id="dff03-102">RaiseError macro action</span></span>

<span data-ttu-id="dff03-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dff03-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="dff03-104">L'action **DéclencherErreur** lève une exception qui peut être gérée par l'action de macro **[SurErreur](onerror-macro-action.md)**.</span><span class="sxs-lookup"><span data-stu-id="dff03-104">The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.</span></span>

> [!NOTE]
> <span data-ttu-id="dff03-105">[!REMARQUE] L'action **DéclencherErreur** est disponible uniquement dans les macros de données.</span><span class="sxs-lookup"><span data-stu-id="dff03-105">The **RaiseError** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="dff03-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="dff03-106">Setting</span></span>

<span data-ttu-id="dff03-107">L'action **DéclencherErreur** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="dff03-107">The **RaiseError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dff03-108">Argument</span><span class="sxs-lookup"><span data-stu-id="dff03-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="dff03-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dff03-109">Required</span></span></p></th>
<th><p><span data-ttu-id="dff03-110">Description</span><span class="sxs-lookup"><span data-stu-id="dff03-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dff03-111">Numéro d’erreur</span><span class="sxs-lookup"><span data-stu-id="dff03-111">Error Number</span></span></p></td>
<td><p><span data-ttu-id="dff03-112">Oui</span><span class="sxs-lookup"><span data-stu-id="dff03-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="dff03-113">Nombre ou expression résolu au type de données Long.</span><span class="sxs-lookup"><span data-stu-id="dff03-113">A number or an expression that resolves to the Long data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dff03-114">Description de l’erreur</span><span class="sxs-lookup"><span data-stu-id="dff03-114">Error Description</span></span></p></td>
<td><p><span data-ttu-id="dff03-115">Non</span><span class="sxs-lookup"><span data-stu-id="dff03-115">No</span></span></p></td>
<td><p><span data-ttu-id="dff03-116">Expression de type Chaîne qui décrit l’erreur.</span><span class="sxs-lookup"><span data-stu-id="dff03-116">A string expression that describes the error.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="dff03-117">Notes</span><span class="sxs-lookup"><span data-stu-id="dff03-117">Remarks</span></span>

<span data-ttu-id="dff03-118">Si l'action **DéclencherErreur** est appelée dans un événement de macro **[Avant la modification](before-change-macro-event.md)** ou **[Avant la suppression](before-delete-macro-event.md)**, l'événement est annulé.</span><span class="sxs-lookup"><span data-stu-id="dff03-118">If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.</span></span>

<span data-ttu-id="dff03-p101">S'il n'y a aucune instruction **SurErreur** active qui gère les erreurs, l'erreur levée par l'action **DéclencherErreur** est ajoutée à la table système **USysApplicationLog**. Lorsque l'action **DéclencherErreur** écrit dans la table **USysApplicationLog**, la colonne **Catégorie** prend automatiquement la valeur **Exécution**.</span><span class="sxs-lookup"><span data-stu-id="dff03-p101">If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table. When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.</span></span>

<span data-ttu-id="dff03-121">Pour afficher la table **USysApplicationLog**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="dff03-121">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="dff03-122">Cliquez sur le menu **fichier** , puis cliquez sur **Options**.</span><span class="sxs-lookup"><span data-stu-id="dff03-122">Click the **File** menu, and then click **Options**.</span></span>

2.  <span data-ttu-id="dff03-123">Dans la boîte dialogue **Options Access**, cliquez sur l'onglet **Base de données active**.</span><span class="sxs-lookup"><span data-stu-id="dff03-123">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="dff03-124">Dans la section **Navigation**, cliquez sur **Options de navigation**.</span><span class="sxs-lookup"><span data-stu-id="dff03-124">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="dff03-125">Dans la boîte de dialogue **Options de navigation**, cliquez sur **Afficher les objets système**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="dff03-125">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="dff03-126">Cliquez sur **OK** pour fermer la boîte de dialogue **Options Access**.</span><span class="sxs-lookup"><span data-stu-id="dff03-126">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="dff03-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="dff03-127">Example</span></span>

<span data-ttu-id="dff03-128">L’exemple suivant montre comment utiliser l’action Déclenchererreur pour annuler l’événement de macro de données avant la modification.</span><span class="sxs-lookup"><span data-stu-id="dff03-128">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="dff03-129">Lorsque le champ AssignedTo est mis à jour, un bloc de données RechercherEnregistrement permet de déterminer si le technicien affecté est actuellement affecté à une demande de service en cours.</span><span class="sxs-lookup"><span data-stu-id="dff03-129">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="dff03-130">Si cela est vrai, puis l’événement avant la modification est annulée et l’enregistrement n’est pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="dff03-130">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="dff03-131">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="dff03-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
